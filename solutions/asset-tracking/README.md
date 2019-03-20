# Supply Chain Asset Tracking on Blockchain

## For

* logistics
* manufacturing
* e-commerce \(companies with solid logistics departments\)  

### Need / Benefit

* Product Quality Tracking & Settlement automation to locate the defected goods and process \(e.g. recall\) other defected products
  * Automate fraud-detection cases
  * Transparent composition of ingredients and  follow of the entire chain
  * Representing the immutable information about raw material / product and conditions in which this stuff must be storing / transporting
  * Increase customer confidence \(better detecting the defects and faults\)
  * Traceability and easy detection of the current assets location and replacement  
  * Ensuring the parameters compliance & standards
  * Achieve traceability information about the full supply chain conditions / raw materials the product made of each ERC721 token
* Restricted access to the data  that should be shown to members  based on the specific types of users
* Cost effective solution per transaction
* Storage solution for photo and documents
* Oracle
* Scalability with the high-load performance
* IoT integration

An estimated, 75% of available supply chain data originates from outside the ERP system. Complexity opens risks of miscommunication and disruptions, often from incorrect or incomplete data.

According to a 2018 survey by GEODIS, only 6% of 623 supply chain professionals across 17 countries think they have adequate supply chain visibility.

* [https://www.supplychain247.com/article/top\_supply\_chain\_planning\_challenges](https://www.supplychain247.com/article/top_supply_chain_planning_challenges%20)
* [https://www.mckinsey.com/business-functions/operations/our-insights/blockchain-technology-for-supply-chainsa-must-or-a-maybe](https://www.mckinsey.com/business-functions/operations/our-insights/blockchain-technology-for-supply-chainsa-must-or-a-maybe
  )
* [https://www.supplychain247.com/paper/solving\_the\_supply\_chain\_planning\_puzzle/logility](https://www.supplychain247.com/paper/solving_the_supply_chain_planning_puzzle/logility)

## Solution / Specifications

System for the tracking  traceability of the producing and distribution outputs:

* Dashboards for producers, traders, certifiers, manufacturers and consumers;
* Effective traceability of the metadata \(metrics\) and automatization audit of the shipment conditions;
* Enhance the monitoring capability due to lack of transparency in the multi supply chain system and inefficient processes ;
* Automatization the process due to tokenizing the assets;
* Tamper-proof data to build trust among parties;

### Blockchain & Data Sharing

#### Immutability

* Immutability of the records for the multi-actors supply chain system  \(immutable history of the modifications\)
* The ledger’s consistency is enforced based on the selected consensus implementation
* The private  network is scalable solution and could  to include as many participants as needed when the supply chain network grows
* Permission to join the distributed ledger as a peer organization
* Avoiding the possibility to attach the fake history for the supply history

#### Data Sharing

* Have the ability to partially share private information like addresses to another participant in the system and guarantee the identity on the platform.
* Don’t share all information about owning goods and volumes publicly.
* Don’t share private information about deals publicly

#### Hyperledger Fabric for blockchain layer

In most cases Hyperledger Fabric as compatible blockchain solution allows an organization to participate in multiple, separate blockchain networks via channels and privacy is guaranteed by channels, so each user role may have own access data rules.

1. It has ability to define ‘channels' for complete data isolation between a set of participants \(organizations\), where each channel is essentially its own private blockchain.
2. It has ability to use 'private data collections’ when participants need to transact on the same blockchain, but keep data private to a subset of transactors \(and potentially regulators/auditors\).
3. It has the ability to utilize Identity Mixer to preserve the anonymity of transaction submitters.

![Hyperledger Fabric / private data management](https://lh6.googleusercontent.com/8avIMb6G2sr6wYYZENaDSeTqUWSLyU-U1MQf_WG7fdSYzk9QzW1wzq5J3XDmn4hd9Z_mjZtrRUEY7S0K5ZVSfMU0qhWwmSgwZafwchdCr4FUK73Wl3soodFRluHzv86apIglO2nI)

How could you ensure the traceability for the participants of the network?

The diagram displays workflow for producing new assets, split, transfer and merge several assets into a new asset, also shows how traceability achieves.

#### Other compatible blockchain solutions for supply chain

After reviewing the specs, we were considering the Hyperledger Sawtooth and Fabric as  compatible blockchain solution

In comparison to Hyperledger Sawtooth, - peers have access to all transaction data. Here is possible to encrypt data and use Hyperledger Sawtooth, but there are risks in future that data can be decrypted.

Hyperledger Fabric, provide  multiple levels of privacy that Sawtooth doesn't have. All peers in Sawtooth have the full copy of the ledgers, however in Fabric it allows to have access by channels. It allows the reflect the specific data for the members of the network.

Ready white label solutions

* [Over Haul](https://over-haul.com/solutions-overview/)
* [DL Asset Track](https://dltlabs.com/products/#dl-asset-track)

Competitors samples

* [Sigma Ledger](https://www.sigmaledger.com/)
* [ScanTrust](https://www.scantrust.com/)
* [OnFleet](https://onfleet.com/)

### Components

The components of the system for traceability  he system for improving the traceability for specific use case in the supply chain of the manufacturing and trading processes

* Storage
* Sharing private information
* Traceability of goods
* Managing organizations
* Managing employees in organizations
* Assets

#### Constraints

* Integration with existing system via API
* Hyperledger Fabric for the blockchain part
* Cloud infrastructure  as a cloud service for Fabric and backend storage

### MVP Scope

#### Roles

* Producer
* Manufacturer
* Trader/Retailer
* End Customer
* Certifier

#### Features

* Create Account 
* Identity
* Create/Transfer 
* Time Stamp and Geo location
* History 

## Publications

* [Supply Chain Blockchain Tech Review & Comparison](supply-chain-blockchain-tech-review-and-comparison.md)
* [RecycleChain – a concept of a blockchain platform for open market in the waste management space](https://medium.com/practical-blockchain/recyclechain-whitepaper-76e792182df0)

