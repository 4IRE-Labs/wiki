# Supply Chain Asset Tracking

### For

* logistics
* manufacturing
* e-commerce \(companies with solid logistics departments\)  

### Need / Benefit

* Product Quality Tracking & Settlement automation to locate the defected goods and process \(e.g. recall\) other defected products
  * Immutability of the records for the multi-actors supply chain system  \(immutable history of the modifications\)
  * The ledger’s consistency is enforced based on the selected consensus implementation
  * The private  network is scalable solution and could  to include as many participants as needed when the supply chain network grows
  * Permission to join the distributed ledger as a peer organization
  * Avoiding the possibility to attach the fake history for the supply history  

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

### Ensuring the transparent traceability

1. Automate fraud-detection cases
2. Transparent composition of ingredients and  follow of the entire chain
3. Representing the immutable information about raw material / product and conditions in which this stuff must be storing / transporting
4. Increase customer confidence \(better detecting the defects and faults\)
5. Traceability and easy detection of the current assets location and replacement  
6. Ensuring the parameters compliance & standards
7. Achieve traceability information about the full supply chain conditions / raw materials the product made of each ERC721 token

The components of the system for traceability  he system for improving the traceability for specific use case in the supply chain of the manufacturing and trading processes

1. Storage
2. Sharing private information
3. Traceability of goods
4. Managing organizations
5. Managing employees in organizations
6. Assets

### Permissioned Blockchain & Private Data

* Have the ability to partially share private information like addresses to another participant in the system and guarantee the identity on the platform.
* Don’t share all information about owning goods and volumes publicly.
* Don’t share private information about deals publicly

We consider the Hyperledger Fabric as compatible blockchain solution that allows an organization to participate in multiple, separate blockchain networks via channels and privacy is guaranteed by channels, so each user role may have own access data rules.

![Hyperledger Fabric / private data management](https://lh6.googleusercontent.com/8avIMb6G2sr6wYYZENaDSeTqUWSLyU-U1MQf_WG7fdSYzk9QzW1wzq5J3XDmn4hd9Z_mjZtrRUEY7S0K5ZVSfMU0qhWwmSgwZafwchdCr4FUK73Wl3soodFRluHzv86apIglO2nI)

How could you ensure the traceability for the participants of the network?  
****

![](https://lh4.googleusercontent.com/kbuF4iQIRkHOV_Vgy2c2j_cdgpUVbzeGwDbevlJY-pMryrswudalbwENFd_qW1RvCTWBH3NRDBQP8jgPn7z_apKAJASPbZGwcPl3mrpqSt-0p4oR_yKX6-ibrklWqYV7lfDrGszn)

The diagram displays workflow for producing new assets, split, transfer and merge several assets into a new asset, also shows how traceability achieves.

### Other compatible blockchain solutions for supply chain

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

## Publications

* [Supply Chain Blockchain Tech Review & Comparison](supply-chain-blockchain-tech-review-and-comparison.md)
* [RecycleChain – a concept of a blockchain platform for open market in the waste management space](https://medium.com/practical-blockchain/recyclechain-whitepaper-76e792182df0)

