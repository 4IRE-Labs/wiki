# Implementation Handbook

## Process for the client

1. Provide ICO General Info \(below\)
2. Provide ETH address for collecting the funds
3. Provide access to domain, AWS, CRM, Support and other 3rd party services \(if applicable\)
4. Provide credentials for KYC \(if applicable\)
5. Top up the smart contract address with ethereum ~$100

The usual process of setup takes 2 weeks, including communication delays, syncing the nodes, design update and smart contracts publishing.

## ICO General Info <a id="ICOStartingRequirements-ICOGeneralInfo"></a>

List of things to be clarified before starting production run of new ICO.

| Input | Value |
| :--- | :--- |
| Token Full Name  | e.g. Icon Token |
| Token Short Name \(e.g. ICX\) | e.g. ICX |
| Start Date/Time |  |
| End Date/Time |  |
| ETH to Token Ration \(e.g. 1456 tokens per ETH\) | e.g. 1456 tokens per 1 ETH |
| ETH Crowdsale Goal/Cap  | \(hard cap, soft cap\) |
| Beneficiary wallet address |  |



## Monitoring Metrics

### On Application Servers

* Requests per second
* Errors per second
* Request duration
* Background workers queue size
* Background workers job duration
* Also lots of system metrics like amount of DB requests, etc

### On Crypto Nodes

* Free Space
* CPU Usage
* RAM Usage

### External monitoring

* Crypto nodes availability over JSON-RPC
* Separate monitoring of unhandled exceptions
* Website availability monitoring

### Triggers

All triggers on actions above notify support team, not doing some automated actions to apps.

## 3rd party services

* [Amazon Web Services](https://aws.amazon.com/) EC2 ~$500-600 / mo.
* [Sentry](https://sentry.io/) – $30 / mo.
* [Pingdom](https://www.pingdom.com/) – $15 / mo.
* [Mailguin](https://mailgun.com) – $80 / mo.
* [Shapeshift](https://shapeshift.io/) \(for exchange\) – free
* [Coinbase](https://www.coinbase.com/) \(for rates\) – free
* [Zendesk](https://www.zendesk.com) \(support\) – $25+
* [Artemis](https://www.cynopsis-solutions.com/artemis) or [Onfido](https://onfido.com/) \(KYC\) – optional, price vary cents to dollars per check
* [Drip](https://www.drip.com/) \(CRM, optional\) - $49+

## Security Techinques

* 2-factor authentication for admin access.
* Encryption of stored sensitive data \(KYC profiles, eth wallet private key\). Encrypted with Fernet algorithm. Decryption keyus stored in app server's environment variables.
* SSL encryption for users
* Using virtual private network between all nodes. Public services exposed via load-balancers.
* Using managed data store \(Amazon RDS\)
* Deployment project with sensitive variables stored in the separate repo
* Reachability to crypto nodes protected by firewall
* BTC node is encrypted by passphrase and we don't store it in our environment
* For authentication we use JWT, so we don't store any tokens on backend side

