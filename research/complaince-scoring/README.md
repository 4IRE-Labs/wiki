# Compliance Automation

For services working with crypto payments

### Problem Definition

* Converting to FIAT through the bank for crypto businesses \(they can freeze, as they can't verify the source of funds\)
* Simplify the compliance check-up for crypto businesses \(exchanges have big compliance deps, e.g. CEO has 40 people\)

### Existing solutions

* [Bitfury Crystal](https://crystalblockchain.com/)
* [Coinfirm](https://www.coinfirm.com) \([example report](https://drive.google.com/open?id=1Nuxbz_E9k9VxLifZUO0yhEna9tHOgr4g)\) – show status, but don't provide info for proper compliance
* [Chainalysis](https://www.chainalysis.com/)
* [Wyre](http://sendwyre.com/) \(has compliance module\)
* [heycoral](https://heycoral.com/)

### Potential Solution

* Mark verified sources
* Best markets for regulation: Switzerland, Singapore, US \(maybe\) 

### Tasks

* Define solution and show Axons for review and additions
* Ask banks what they find sufficient

## Binance SAFU Challenge

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

### SAFU Solution 1

Approach**:** As bad actors can easily create new addresses we suggest to measure positive rating instead of negative. E.g. adding points for transaction history based on volume and frequency on the on side. And add extra for reputation of transacting addresses as well, e.g. if this wallet was transacting with a known exchange, that does KYC – it gives a bonus to credibility. Also connecting you social media with the wallet \(by posting a code like in Keybase\) can also give extra points. Ideally we want to hide the connection with the specific profile and rather just prove that the connection exists.

Then add an ability to send a red flag to the given address. So other addresses with a good rating can notify the scam nature of this address and maybe attach the link or document with details. So API should not only show the rating but also the list of such claims. We don’t see a viable way to incentivize the flagging. For usual users it’s not a frequent situation and micropayment won’t be a sufficient motivator. The desire to black list may be enough. Incentivization can work for organizations like exchanges. So they’ll create a fund and distribute the fees earned based on the number of scammers found in the API searches \(so they’ll earn only if they prevent the transaction\).

Exchange like Binance can limit the withdrawals for wallets without history or having red flags.

Goto market: make a small prototype, setup demos/interview meetings with major players, specifically their compliance roles. Offer some trial period and try to sign with 2-5 players first. Collect the stats for the future case.

Scaling: present widely the results of the case in media and conferences. Open up automated sign up service.

### SAFU Solution **2**

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

