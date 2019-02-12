# Enabling fast, transparent and compliant cross-border payments with the blockchain

For: Remittance services \(Western Union, Transferwise, UAE Exchange [long list](https://www.remitrate.com/money-transfer-companies)\)

Enabling fast, transparent and compliant cross-border payments with the blockchain

## Business Context

* Transparency and immutability of ledger – key attribute of the system that creates trust between service, investors and regulators.
* Investors can provide liquidity in domestic banks
* PSD2 for cheap remittance
* Dashboards for accountants and regulators
* KYC

### Why blockchain

* Unmodifiable, verified transaction records store the entire structured history forever
* Provenance, resistance to forges, and transaction transparency are the core properties of the ledger protected with cryptographic hash links and physically replicated to all the participating enterprises
* The ledger’s consistency is enforced based on the selected consensus implementation
* The network is unlimitedly scalable to include as many participants as needed when the supply chain network grows
* Permission to join the distributed ledger as a peer organization is controlled by the standardization committee or a similar collegial entity.

### Business value

The blockchain technology introduces the following core benefits for this product:

* Provide cryptographic-proven immutable history to the end users, intermediaries, investors and regulators
* Ability to automate fraud-detection cases based on ledger’s history
* Ability to automate business processes based on smart contracts feature – trigger particular event in the system when certain conditions are met
* Ability to control data visibility for parties involved into the transactions via channels
* Ability to easy open data for new parties

### Constraints

* Integration with banks for cheap remittances via PSD2 TPP
* EVM based blockchain
* The backend is running on a cloud infrastructure

## Concept

### Quorum

* Built and open sourced by J.P. Morgan
* Based on Ethereum \(Largest Ecosystem of Developers, Tools, DApps\)
* Reliable, fast enough for remittance case and scalable
* Has replaceable consensus algorithm
* Production since July 2015.
* Supported by the biggest blockchain community \(Ethereum\)
* Implementation is stable and mature with extensive documentation and vibrant community \(50,000+ unit tests, Security Audits, Bounty Program\)
* Client SDKs \(Web3\) are available for most popular programming ecosystems including Java, Python, .NET and JavaScript
* Suites well the consortium-like blockchain network configuration

### Stellar

TBD  


### Use case refinement

![](https://lh6.googleusercontent.com/Ht__AFDeWUK_g2CaD0ZfsgvQMKscOJOISIV-Fv0xcvHZmi34_h1iWJHhVuuRj5NCO9EVsunfpZtVfoGtpHivIoTSUG4N9nXaQf8wUSthfiJwU2y6movh5lkvmIMEGlIqqBKT3mA7)

### Solution Proposal

* Create remittance system based on DLT for immutability and auditability
* JP Morgan Quorum is used for blockchain solution;
* Network peers \(nodes\) are divided by user-roles:
  * CaponeResearch - provides the service
  * Investors - provides liquidity
  * Regulators - for auditability
* Transactions processing is based on EVM events
* Domestic remittances initiated via TPP PSD2 integration with Banks\*
* Custom analytics is built on top of the blockchain part
* CaponeResearch nodes are maintained on Kaleido platofrm
* Parties \(investors/regulators\) peers may be provided as a service both inside \(kaleido\) / outside infrastructure\*\*  
* The implementation starts with PoC and extended with a new functionality on demand;

\* provide peers as a service in cloud \(kaleido\)s or on premise should be discussed separately

\*\* support only 2 banks in PoC

### What is Unique Value

The proposed reference architecture addresses the following key quality attributes:

* Security – cryptography protected history stored on different peers;
* Immutability – once event is captured it’s no longer can be changed;
* Auditability – in case of disputes between parties \(end user – bank – investor\) ledger history will be used as a trusted proof; any manual human-related action \(e.g. manual accountant work in case of the false-positive failure detected by the system\) is captured and easily verified later.

### Architecture Explained

* The CaponeResearch \(CR\) system operates as TPP \(3rd party payment provider\) in EU. It triggers Bob’s bank API to initiate transaction from his bank to CR’s domestic bank.
* Once CR’s domestic bank received a payment, it updates transaction by triggering smart-contract on Quorum’s blockchain.
* Every time transaction is updated on the blockchain the smart-contract emits the appropriate event.
* As these events are private they are broadcasted to the blockchain peers via Tessera component of Quorum.
* CR backend has workers that are polling smart-contract for new events and execute appropriate business logic when an event is received.

### What is captured via blockchain

Since blockchain is considered as an audit trail log for the system it may capture the following data:

* Emittance requests
* Bob’s transaction confirmations
* Transactions between Bob’s bank and CR’s domestic bank
* Transactions between CR’s domestic bank and Alice’s bank

Although, all transaction will be visible only to regulator role, service role and banks participated in the transaction.  


Blockchain transaction may not contain Bob’s and Alice’s identity and privacy data and will store only a reference id to the corresponding data in the original storage. All transactions have timestamps and protected by cryptography.  


## Solution Context views

![](https://lh6.googleusercontent.com/xtS4ruNxOEObgKdOEcpLAMCxAhp0ztLBHljWhj7nTFHZzAuyQ4SD732cKYqfDprXcJgJFyIquQoA4mkNvQagn-K5gY8kVm4b8XUxhUTucFDMcaBVIOdrnw1nmd_dHvQ9faN0nX3C)

### Integration Explained

### Context

1. Update transaction / remittance request state on the blockchain
2. Process transactions based on events received from the blockchain
3. Store users identities in local-storage only
4. Move payment processing into separate service

### Benefits

1. Data is captured into the blockchain on the earliest possible stage
2. Local storage cannot run out of sync with ledger
3. GDPR compliance
4. Simple integration of new banks via OpenBanking

### Further network extension

* Internal blockchain usage for different user-roles is not the only way to track shipments
* Other payment partners can be integrated via shared process based on smart-contracts
* Information stored outside the system is captured to extend the horizons of the tracked history;

## POC Implementation scope

The main suggestion is to start with PoC implementation which will contain:

1. Consortia blockchain with management system via Kaleido
2. Payment processing with APIs of 2 banks
3. Identity service with KYC
4. Website frontend
5. Bank’s and regulator’s nodes are out of scope
6. Analytics system is out of scope
7. Blockexplorer integrated into Kaleido

## Summary

The blockchain naturally fits business case for cross-border remittances to:

* Capture immutable and verifiable log of events
* Be used in case of disputes between different parties – users, banks, investors, regulators via history traceability
* The blockchain solution integration process is divided into two milestones:
* PoC implementation – vertically scalable prototype
* Further evolution of blockchain part with all required events captured

