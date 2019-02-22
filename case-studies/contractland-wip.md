# Contractland

Protocol for interchain transfers between Ethereum and Bitcoin

Problem: there were no mechanism for establishing in details the mechanism for permission-less transferring of assets between Ethereum and Bitcoin.

Services: [Architecture / Protocol Design](../services/architecture-design-protocol.md)

Team: [Kirill Kirikov](../org/credentials-wip/kirill-kirikov.md)

**SOLUTION**

![](../.gitbook/assets/image%20%2849%29.png)

We’ve design the bridge, that is a two way pegging mechanism that works through a rotating validator set and two bridge contracts \(“contract” here refers to an executable piece of logic in the context of its residing chain\). The bridge contracts resides on the home and foreign chains, hereon referred to as home-bridge and foreign-bridge.

This solution could be useful in fields such as: Stable coins: External chain assets such as BTC could diversify the collaterals used in stable currencies on Ethereum Decentralized exchanges: Ability to transfer external assets onto Ethereum expands the available assets for trading Financial derivatives: Interconnecting blockchain based assets opens up possibilities for various financial derivative products.

## Consensus

Any transfer requests with approval from _N/2 + 1_ validators are finalized. This process continues indefinitely unless _N/2_ or more validators become unresponsive, in which case the bridge halts.

## Security Assumptions

The bridge is secure as long as the attacker controls less than 51% of the validator pool.

## Home \(Ethereum\) Bridge Implementation

The home bridge will be written in Solidity and ran on EVM.

The home bridge will have the following interface:

* `transferToForeign(string recipient, uint amount, bytes32 uniqueId)`
* `transferFromForeign(address recipient, bytes rawTxOut)`

Events:

* `TransferToForeign (string recipient, uint256 value, bytes32 uniqueId)`
* `TransferFromForeign(address recipient, uint256 value, bytes32 txId)`
* `SignedForTransferFromForeign(address indexed signer, bytes32 txId)`

### Transferring Funds

* Dapps or contracts could call the function `transferToForeign` to withdraw their BTC from home-bridge to the provided BTC address, and listen TransferToForeign for transfer results.

### Home Token

* The pegged token used on home chain to represent foreign token aka HomeToken will be a [Mintable](https://github.com/OpenZeppelin/openzeppelin-solidity/blob/v1.12.0/contracts/token/ERC20/MintableToken.sol) and [Burnable](https://github.com/OpenZeppelin/openzeppelin-solidity/blob/v1.12.0/contracts/token/ERC20/BurnableToken.sol) ERC20 token. The mintable and burnable properties or the token allows easy management of the pegged token. It can be transferred to the home bridge and destoryed on transfer outs \(to foreign\), and created and sent to recipient on transfer ins \(from foreign\).

### Selecting outputs that could be spent to transfer BTC from foreign-bridge

* Transfer funds in bitcoin terms is called: spending of output. In our case, output - is one of the bitcoin transactions that has output pointing to the foreign-bridge. To send money to the recipient, validators must agree on the transaction outputs to be spent and sign them. As home-bridge keeps track of all incoming and outcoming transactions on the foreign-bridge then it can determine the outputs that could be spent for the given message.

### Signign outputs and verifying signature

* These outputs will be combined in the transaction and signed to get witnesses and must be pushed to the home-bridge by calling `submitSignature(bytes witness, bytes rawTx, bytes32 requestId)`.

  * `rawTx` is raw unsigned transaction provided by validator that is used to create a signature. [See it's structure](https://github.com/bitcoinjs/bitcoinjs-lib/blob/f57a73496d5a1dec54dffdb3936d5dd63a15b4fe/src/transaction.js#L319)

  ```text
    (version) = 2
    (hashPrevouts) => hash256(txIns.hash + txIns.index)
    (hashSequence) => hash256(txIns.sequence)
    (input.hash) txId in little-endian
    (input.index)
    (prevOutScript) multisig redeem script
    (value)
    (input.sequence) default sequence 0xffffffff
    (hashOutputs) => hash256(out.value + out.script)
    (this.locktime) => 0
    (hashType) => 1 SIGHASH_ALL
  ```

  * `witness` - is a `rawTx` signed with validator's private key and it will be used to unlock funds on the foreign-bridge.
  * `requestId` - is needed to understand what output was blocked for current witdrawal request

### How to create witness

To get the witness validator must create a transaction with the following params:

* inputs is an array:

```text
  [
    {
        'txid': txOutput['txid'],
        'vout': txOutput['vout']
    }
  ]
```

* outputs is an array:

```text
  [
    {
        recipientAddress: amountToSend
    },
    {
        foreignBridgeAddress: change
    },
    {
        rewardsMultisigAddress: validatorReward
    }
  ]
```

One of the possible methods to create the unsigned transaction is execute bitcoind rpc method `createrawtransaction(inputs, outputs)`. Then this transaction must be signed with validator's private key. Possible method of signing the transaction is using bitcoind rpc method `signrawtransactionwithkey(unsigned, [validatorPrivateKey], prevTxs)`. The `prevTxs` is an array of transactions that outputs will be spent. The `signrawtransaction` returns transaction with witness in it.

