# KYC module integartion

**KYC module integration**

For whom:

* hybrid digital wallets 
* fintech service provider needed the automatic Online & Biometric Identity Verification \(KYC\)  for b2b and b2c users 
* fintech startups that should meet the banks' KYC requirements
* crypto exchanges



### **1st option**

Using 725/730  ERC token standards with the further KYC provider integration \(using the smart contracts\) based on our [case study for notary on blockchain](https://wiki.4irelabs.com/docs/solutions/asset-tracking/notarization-platform).   
****

**Cons:**

* complexity for the users while on-boarding process
* compatible only for Ethereum based Dapps
* 725 / 730 ERC token is under development and discussion by the community

**Benefits:**

* easy integration with the other KYC \( ID service \) providers
* verifying identity on-chain / off-chain

**There are roles while transferring funds:**

* Consumer - one of the participants who take part in transferring funds
* Service Provider - an entity which provides service and infrastructure for funds transferring.
* Certificate authority - an entity which is accredited by Service Provider to verify identities and provide proofs about them.

**Identity Verification flow overview:**

1. Certificate authority deploys its own identity contract.
2. Certificate authority adds a CLAIM key to its identity contract.
3. Consumer deploys their identity contract.
4. After Consumer successfully undergoes identity verification, Certificate authority signs an identity claim for Consumer.
5. The consumer adds Certificate authority’s signed claim to their identity contract.
6. Service Provider deploys it’s contracts for transaction management \(Coordinator Smart Contract...\).
7. The consumer uses the services provided by the platform \( Provider\) through their identity contract to Service Provider’s contracts.
8. Service Provider’s contract confirms that the Consumer’s identity contract contains a claim by a Certificate authority before doing any changes.

### **2nd option**

**integration with the several local and global KYC providers**  


The more complex verification process

We could recommend several local KYC local providers and also add the global KYC provider with a good worldwide reputation \( like [thomsonreuters.com](https://www.thomsonreuters.com/en.html)  for verifying the blacklist countries, terrorists, etc\)  


Benefits:

* adding new KYC providers in the future
* more complex verification process

The verification process also differs in Asia as the local ID providers claim 

* **Streaming:** __Voice and face identification via video chat 

We also assisted the fintech startup with the KYC process and it was implemented under 3 steps \( for EU based customers\) :

- verify the identity via ****[**https://www.passfort.com**](https://www.passfort.com)

**-** verify the address via 3rd party service integration

- for transactions up to 50 K the user should provide the source of the funds, conduct the passport verification and manually change the status via the admin panel\)

For each KYC verification is paid commission. The main challenge was related to non-relevant passport photos or selfies, thus it was decided to integrate AI based solution for filtering the photos instead of paying commission for non-relevant verifications to KYC providers. Artificial intelligence was used for approvement of documents via self-learning algorithms.  
****

**For both options, we can use the KYC module of our crowdfunding platform:**

* UI customer and admin
* backend logic for data encryption and uploading to the KYC providers

![](https://lh3.googleusercontent.com/UHgxNKaVqor_M1kefbMwrM0HmAjGIOnkx_zL_WYZ6AKqOpe9y70q9OFgeUzR1FBm7ynLL4MpcUABjZYzyg8JAdfawSWePDtV-gp1O-aqjLHyE31bXmnEZD2XwKf0C4iWjNaTV_Ui)

We also worked with APIs of well-know KYC providers while we were integrating them to our product.

* [https://sumsub.com/](https://sumsub.com/)
* [https://onfido.com/](https://onfido.com/)
* [https://www.cynopsis-solutions.com/artemis](https://www.cynopsis-solutions.com/artemis)
* [https://www.thomsonreuters.com](https://www.thomsonreuters.com/en.html)

Useful info on:

{% embed url="https://medium.com/trimplement/the-fintech-kyc-compliance-guide-48ccaed984c0" %}

\

{% embed url="https://www.slimpay.com/blog/what-is-kyc/" %}



