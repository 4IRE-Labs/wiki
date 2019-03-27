# RecycleChain for Smart City Waste Management

RecycleChain is a concept of a blockchain platform for open market in the waste management space.

### Problem

* Low Waste sorting rate between people in developing countries
* No incentives \(positive or negative\)
* Doesn’t connect further \(houses, districts, cities\)
* Lack of culture, knowledge
* Distribution centers are unattractive: unkown, unstable, have lots of bums
* Underload of the recycling factories
* Low Margins = Intermediary & supply chain efficiency
* Low capacity storages
* Good recyclables are stolen in the chain
* Low municipal tariff
* Corruption on the high level

## Solution & Product

### **Abstract**

RecycleChain is an open market for recyclables. Core of the system is the blockchain database, that’s stored and synced between all users. It will hold next data:

* Amount, type and price of waste in possession of each player
* Ownership transactions in a form of smart contracts \[1\]
* Trading balance in the internal blockchain currency \(cryptocurrency\)

![](https://cdn-images-1.medium.com/max/1600/0*W4ybBPAk6svy5Zhx.)

It brings next benefits.

### **For Households**

* Incentive to separate recyclables
* Transparency around the process

### **For distribution centers / businesses**

* Buy/Sell recyclables for better price
* Identify opportunities \(new collection spots\)

### **For Governments**

* Is autonomous \(independent\) and brings the trust layer
* Incentivizes players to track and sell their recyclables
* Allows new players to connect to the economy \(distributions centers, deliveries, small recycling facilities\)
* Allows efficient side funding
* Secure, Reliable & Easy to scale infrastructure
* Auditable for government

## **Case studies**

[**Plastic Bank**](https://www.plasticbank.org/) is a platform for the world to Gather Together to alleviate global poverty and Ocean Plastic. It is a convenience store for the worlds poor that accepts plastic waste as a currency, and is sustained through the use of Social Plastic.

Working with Cognition Foundry, the Plastic Bank leverages the best technology, allowing them to grow exponentially while maintaining security of transactions. Blockchain provides trust in an industry that has been fraught with corruption and danger; it provides trust to “recyclers” that their data is safe, they are safe, and their finances are safe. [More](https://www.ibm.com/blogs/systems/plastic-bank-deploys-blockchain-to-reduce-ocean-plastic/)

**The Dnepr Regional Council** approved a new strategy for handling solid domestic waste. It allows to pay for the removal and disposal of waste by the waste itself. Citizens will take the waste for recycling at special centers and receive a cashback on a special card which you can use to pay for the utility bills. [More \(in russian\)](https://uteka.ua/publication/Za-kommunalnye-platezhi-mozhno-budet-rasschitatsya-musorom)

## **Architecture**

The core of the system is the blockchain database.

A blockchain — is a continuously growing list of records, called blocks, which are linked and secured using cryptography. Each block typically contains a hash pointer as a link to a previous block, a timestamp and transaction data. By design, blockchains are inherently resistant to modification of the data. A blockchain can serve as “an open, distributed ledger that can record transactions between two parties efficiently and in a verifiable and permanent way. For use as a distributed ledger a blockchain is typically managed by a peer-to-peer network collectively adhering to a protocol for validating new blocks. Once recorded, the data in any given block cannot be altered retroactively without the alteration of all subsequent blocks, which needs a collusion of the network majority. \(Wikipedia\)

For the blockchain tech was chosen Ethereum, as a widely used technology that also allow the smart contracts functionality from the box. There’s an additional layer on node.js for registrations and storing additional info. Backend provides API for the mobile app.

Current mobile application allow to interact between the households and distribution centers. You can preview the interface here: [https://invis.io/QWDMQ09N5](https://invis.io/QWDMQ09N5)

## **Notes**

1. Smart contract is an agreement performed in the code, specific example — automatically transfers owners rights to some object to the user who sends funds
2. [Presentation](https://docs.google.com/presentation/d/e/2PACX-1vTs1ZB5aK4sA5FMqRZodEnXeyGo9NcwA_NCdvwPs6czJkGueaXk2-NxP4iluFXaEbUkCeSYDWsYJo0D/pub?start=false&loop=false&delayms=3000) from the Blockchain Hackathon

