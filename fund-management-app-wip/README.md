# Fund Management App \(WIP\)

### Customer Segments

Startup founders

Early adopters: Crypro entreprenurs

### Problem / Need

Collect funding

Alternatives: 

* [https://coinlaunch.market/](https://coinlaunch.market/)
* [https://www.kickico.com/](https://www.kickico.com/)
* [https://icoyard.io/](https://icoyard.io/)
* [https://melonport.com/](https://melonport.com/)

## Key Features

* Setup Multisig
* Launch Token
* Direct \(PreSale\) Distribution
* Mass Distribution

old:

## Roadmap <a id="roadmap"></a>

### v 1.3 \(Current\) <a id="v-1-3-current"></a>

* Token generation and crowdsale smart contracts \(ICO stages, soft / hard cap, discounts\)
* Accept ETH, BTC
* Accept other coins via ShapeShift
* Manual deposits \(e.g. from bankwire\)
* Account - sign in with email, password reset, auto-logout,
* Transaction History
* Multi-level Referral program
* Whitelists
* KYC provider integration \(Onfido, Cynopsis\)
* Google Analytics
* Server monitoring and alerting
* DDoS protection \(Cloudflare\)
* UI Themes: White-label solution with customizable design
* Multilanguage
* 2FA Admin Login
* Token Swaps between users
* Integration with CRM \(Drip.com\)
* Translation Management

### v 1.4 \(Sep 1st\) <a id="v-1-4-sep-1st"></a>

* Token withdrawal limitation and vesting
* Analytics dashboard for ICO management

## Investor Panel <a id="investor-panel"></a>

### Sign up <a id="sign-up"></a>

1. User enters email
2. User confirms email
3. User logins with password sent to email
4. User fills in the KYC form
5. User gets notification on the approval or rejext
6. User can see the invest functionality

## ICO Manager Panel <a id="ico-manager-panel"></a>

### Translation Management <a id="translation-management"></a>

We provide a panel where any new languages can be added to the system on the fly.

### BTC Storage and Withdraw <a id="btc-storage-and-withdraw"></a>

While in Ethereum all funds go to 1 address, the BTC is a bit more complicated.

On our server we run a BTC node and account with lots of precreated addresses that would be assigned for each user. While account hold all BTC and owner can do transactions from any wallet is's undesirable to do such out of ICONX.

Thus to avoid this we treat this address as an temporary storage and give option in our admin panel to withdraw from it at any time. By using this feature, funds from all addresses are collected and send to ICO manager designated wallet with 1 transaction.

In order for the ICO manager to maintain full control over that funds he can encrypt the BTC node with his password in the Admin Panel. Thus only by having this password transactions are possible.

Auto-Send is not done to a\) preserve commissions and b\) manual transactions may still be needed if a big investment comes.

## Key Metrics



## Financials

