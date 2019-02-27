# Cross-border payments

For:

* Remittance services \(SWIFT, Western Union, Transferwise, UAE Exchange [long list](https://www.remitrate.com/money-transfer-companies)\)
* Export/Import settlements
* Smart banking solutions / financial groups \(eg. rubixfinancila\)
* Crypto wallets \(for cashing out in the local currency\)
* Foreign Exchange Platforms
* Brokers

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
  * Remittance Service - provides the service
  * Investors - provides liquidity
  * Regulators - for auditability
* Transactions processing is based on EVM events
* Domestic remittances initiated via TPP PSD2 integration with Banks\*
* Custom analytics is built on top of the blockchain part
* Remittance Service nodes are maintained on Kaleido platofrm
* Parties \(investors/regulators\) peers may be provided as a service both inside \(kaleido\) / outside infrastructure\*\*  
* The implementation starts with PoC and extended with a new functionality on demand;

\* provide peers as a service in cloud \(kaleido\)s or on premise should be discussed separately

\*\* support only 2 banks in PoC

### What is Unique Value

The proposed reference architecture addresses the following key quality attributes:

* Security – cryptography protected history stored on different peers;
* Immutability – once event is captured it’s no longer can be changed;
* Auditability – in case of disputes between parties \(end user – bank – investor\) ledger history will be used as a trusted proof; any manual human-related action \(e.g. manual accountant work in case of the false-positive failure detected by the system\) is captured and easily verified later.

### What is captured via blockchain

Since blockchain is considered as an audit trail log for the system it may capture the following data:

* Emittance requests
* Bob’s transaction confirmations
* Transactions between Bob’s bank and RS’s domestic bank
* Transactions between RS’s domestic bank and Alice’s bank

Although, all transaction will be visible only to regulator role, service role and banks participated in the transaction.

Blockchain transaction may not contain Bob’s and Alice’s identity and privacy data and will store only a reference id to the corresponding data in the original storage. All transactions have timestamps and protected by cryptography.

## Solution Context views

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

## Case Studies

### SWIFT

The year 2017 started with [SWIFT](https://www.swift.com/news-events/press-releases/swift-explores-blockchain-as-part-of-its-global-payments-innovation-initiative) launching a Proof of Concept \(PoC\) to help banks that are challenged with monitoring and managing their international [nostro accounts](http://www.investopedia.com/terms/n/nostroaccount.asp)—crucial for streamlined cross-border payments. This is a part of SWIFT’s global payments innovation initiative that is looking to set new standards in cross-border payments.

### JPM

Meanwhile J.P. Morgan \([JPM](https://www.nasdaq.com/symbol/jpm)\) launched blockchain-based Interbank Information Network \(IIN\) in collaboration with the Royal Bank of Canada and Australia and New Zealand Banking Group Limited. IIN leverages the distributed ledger technology, or simply blockchain, to minimize friction in the global payments structure by ensuing faster payments in fewer steps but more securely. IIN is powered by [Quorum](https://www.jpmorgan.com/global/Quorum)—an enterprise-focused version of Ethereum developed by JP Morgan. Approximately $5 trillion worth of business payments are processed every day by JP Morgan’s Treasury Services for its clients across more than 100 countries.

### IBM

IBM \([IBM](https://www.nasdaq.com/symbol/ibm)\), which [recently ranked](https://www.juniperresearch.com/press/press-releases/ibm-ranked-no-1-blockchain-technology-leader) as the number one blockchain technology company, announced a blockchain banking solution designed to reduce the settlement time and cost of cross-border payments, customized for businesses and consumers. IBM’s blockchain solution is in collaboration with Stellar.org and KlickEx Group; it is already processing live transactions in 12 currency corridors across the Pacific Islands and Australia, New Zealand and the United Kingdom. 

### Mastercard

The most recent [announcement](https://newsroom.mastercard.com/eu/press-releases/mastercard-opens-up-access-to-blockchain-api-for-partner-banks-and-merchants/) comes from MasterCard \([MA](https://www.nasdaq.com/symbol/ma)\), a prominent name in the payments industry, has opened access to its blockchain technology via its API for partner banks and merchants. MasterCard will begin to implement the technology for business-to-business \(B2B\) space to address challenges of speed, transparency and costs in cross-border payments. MasterCard has been exploring the blockchain technology for some time now and has filed for over 35 patents. It is a member of the Ethereum Enterprise Alliance \(EEA\) and is an investor in the Digital Currency Group.

### Ripple

Additionally, consortiums such as Ripple offer its customers the use of digital asset XRP to process payments anywhere in the world instantly, reliably and at lower costs. [RippleNet](https://ripple.com/files/ripplenet_brochure.pdf), its decentralized global network of banks and payment, boasts of more than 100 financial institution partners.

## Summary

The blockchain naturally fits business case for cross-border remittances to:

* Capture immutable and verifiable log of events
* Be used in case of disputes between different parties – users, banks, investors, regulators via history traceability
* The blockchain solution integration process is divided into two milestones:
* PoC implementation – vertically scalable prototype
* Further evolution of blockchain part with all required events captured

## More info

​[https://www.toptal.com/finance/market-research-analysts/international-money-transfer](https://www.toptal.com/finance/market-research-analysts/international-money-transfer)

