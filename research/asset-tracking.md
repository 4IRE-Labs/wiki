# Asset Tracking \(wip\)

For: Logistics, Manufacturers, Transporation, FMCG etc.

Problem statement: defining a technical solution for

* Settlement automation
* Product Quality Tracking 

## 1.The first option based on Onfleet solution

Review API [http://docs.onfleet.com/docs/authentication](https://www.google.com/url?q=http://docs.onfleet.com/docs/authentication&sa=D&ust=1550156358685000) 

### Positive Points

* Quick start \(SaaS\)
* Already in production
* You don’t need configure own infrastructure
* Well documented API
* Already implemented Dashboard / Analytics additional tools for management
* You don’t need blockchain
* Covers logistic problem
* Metadata lets you annotate many of the API’s entities with your own personalized data. This allows to be flexible in describing

### Negative Points

* Third party service, so some bugs which can be found, can’t be fixed by our team
* Created to solve general problem \(some your needs can be uncovered\) and hard to expand
* Has limitation in requests 20 per sec so you need pay more to extend it
* Hard to integrate own layers like blockchain. To integrate it we can create own backend that will be middleware between onfleet and blockchain layer.
* Covers only logistic part so we need create own implementation for covering the manufacturing process so we will not have one source of true.
* Exists mobile app for driver but can’t be modified for our needs.
* We always need to maintain new versions of OnFleet API.

## 2.  The second solution based on the white label solution + licence fee

As mentioned on a call,  we could suggest considering the ready white-label solution aimed more for tracking the production part that we are partly involved in development with our partner company.

The solution consists of clients platform \( web app\) + client app + admin dashboard.

Currently, system can process 250 K product registrations on daily basis. The ownership is registered via the smart contract. The initially, it was based on IOTA but then it was decided to implement based on the Ethereum for better delivery process automation via the smart contracts.

Technology stack: Node.js, React, Ethereum fork, Docker,

The main problems that solves this solution for businesses:

* the transparent sensors trackability  \(production part\)
* the transparent composition of ingredients in the product / the consignment
* the transparency of the suppliers of the ingredients  
* increase customer confidence \(better detecting the defects and faults\)

The deployment set up is done with using Terraform and Docker. The dev environment is integrated with the Docket container for assuring the full automation.

The possible solutions for usage the white label solution :

* license fee for using the basic package
* license fee + customization + set of the products and sensors for tracking the production process requested by the customer

One of the clients [https://www.sigmaledger.com/](https://www.google.com/url?q=https://www.sigmaledger.com/&sa=D&ust=1550156358689000)

## 3. The third option could be a custom solution based on IOTA or Hyperledger Sawtooth framework

Problem

Lack of transparency/proof of product composition/, increase the customer trust and atomization the delivery process for the high-load system                                         

### Benefits of using the Sawtooth

* custom scalable solution with own infrastructure that could decrease the dev costs
* has the smart contract that could be used for the traceability \( we don't need to write the logic on backend like it would be with IOTA solution as they dont have the smart contracts\)
* stable in case of scalability and use different types of concensys that would increase substantially performance of the system
* using Smart Contracts automatically decline batches of products that were not storing or transferred with appropriate condition
* the complex logic could be written on backend
* compatible solution for projects related with IoT
* permissioned blockchain with different level access to the network for the participants  
* ecosystem based on blockless blockchain
* lightweigh solution         

### Benefits of using the IOTA

* IOTA’s architecture is inherently decentralized
* zero fees for the transaction verification \( verification is done by two randomly chosen transactions in the network.\)
* public blockchain
* compatible solution for projects related with IoT
* processing the high load of the transaction that will assure the stability of IOTA  \( however it will require the stable increase of the participants \)

Comparison of both platforms                                                 

## Proof-of-concept stage                                                

It can be done using Hyperledger Sawtooth or IOTA protocol \(Tange\). Both platforms are developed specifically for IoT and machine economy. There is a small comparison:                                                

### **Hyperledger Sawtooth:**

* started in December 2015 by the Linux Foundation                                
* supported by IBM, Intel and SAP                                                 
* the already existing case for supply chain                                        
* ethereum based Smart Contracts \(using Solidity\)                                        
* open-source                                                                                
* free to use                                                                                 
* transactions fee free                                                        
* only private networks                                                        
* highly modular                                                                        
* well documented                                                                
* big community                                                                
* permission blockchain

### **IOTA Protocol \(Tange\):**

* started in 2015                                                                         
* open-source
* free to use                                                                         
* transactions fee free                                                                
* exist public/test networks                                                        
* permissionless

As it was mentioned above Hyperledger Sawtooth  has the case for the supply chain. It already provides the infrastructure for tracking physical objects in a real-world supply chain on the Sawtooth Ledger. Track and Trade - Provides a methodology for users to track goods as they move through a supply chain. This includes the history of ownership and custodianship, as well as histories for a variety of properties such as temperature and location, weight etc.                                                                                 

