# SAFU Scoring

Approach: We suggest to create a global service that can accept complaints for the public addresses with some sort of witness \(like a screenshot that proves the complaint or filling the form, [see the link](https://www.scamwatch.gov.au/report-a-scam) as an example\). This service in the background will analyze the blockchain transactions that have outputs and inputs pointing to the scam address. The scam score will be given to all addresses in the chain. This score will be calculated depending on the Euclidean distance in the blockchain. Thus, even if user creates the new public address, he wouldn’t have a possibility to use money that he has on other “scam” addresses by sending them to the new address and he will not have possibility to use exchanges which are working with our service. The only possibilities to exchange this funds will be in the gray zone.

The service will provide the information to customers with some set of the text descriptions of the scoring value.

For example:

* Score: 100, Description: “Multiple scam complaints”
* Score: 65, Description: “Address has multiple interactions with scam addresses”
* Score: 50, Description: “The address has small turnover and balance, use carefully”
* … etc

Integrators can use the service just to notify users or even for blocking transactions with big score.

Incentive: We think that people who would consider proofs from complaints must get some pay for their time. Also there should be people who would get money for finding such scams. So our proposition is to setup a fund. The money in different crypto-currencies can be send to this fund from the users of the service on subscription basis.

Goto market: make a small prototype, setup demos/interview meetings with major players, specifically their compliance roles. Offer some trial period and try to sign with 2-5 players first. Collect the stats for the future case.

Scaling: present widely the results of the case in media and conferences. Open up automated sign up service. In future - make the service to be decentralized and working on the blockchain.  


