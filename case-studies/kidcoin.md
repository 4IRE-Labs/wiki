# Kidcoin

**Blockchain-based family finances and digital wallets for kids**

The proven use cases of the dozen released hybrid wallets in Europe and Asia, accelerated the development of different fiat/crypto wallets. We’ve also developed different kinds of wallets but the most exciting was development the hybrid wallet for kids and parents. From business perspective, it is a the app that should facilitate giving, saving, and spending in a family ecosystem. From the tech perspective, it consists of Crypto wallet, FIAT wallet & Debit Card issuing, Allowances and Token Minting. Application is separated into 3 main logical parts: users, financial, blockchain and additional services like micros. The main application server was implemented as a Python/Django application and manages majority of business logic. It’s main logic-heavy part is a financial services \(funds transfer, working with card issuer, and other external APIs, etc\) implemented as Python/Celery. Second logic heavy part is crypto-wallet used primarily to interact with KDC token on Ethereum network. Implemented as Solidity/Truffle/Javascript.  The main goal of this project was improving financial literacy with blockchain thus it seemed to us rather interesting to launch it into life. Our Solution architects design the whole architecture design and interaction between the third party services, crypto wallet and digital cards issuer. The MVP has been already released and currently the project in under continuous development.  


Services: [Architecture / Protocol Design](../services/architecture-design-protocol.md), [Dapps / Wallets Development](../services/dapps-wallets-development.md)

Team: [Kirill Kirikov](../about/kirill-kirikov.md), [Oleg Bugrovoy](../about/oleg-bugrovoy.md)

Technical review, project assessment, solution architecture designing, consulting.

![](../.gitbook/assets/kidcoin_copy.png)

