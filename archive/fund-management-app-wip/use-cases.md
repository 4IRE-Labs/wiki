# Storage

Why you better use Aragon for your Pre-ICO / ICO, even if you're not a DAO

You want to crowdfund, here’s what you’re be dealing with:

* Launch a token
* Setup a secure wallet for funds \(e.g. multisig\)
* Distribute the token \(setup pricing model, payment methods etc\)

Typical situation – select a provider \(see [comparison](https://crowdfunding3.com/resources/ico-platform-comparison)\). What we suggest is to use Aragon:  


<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">ICO wallet</th>
      <th style="text-align:left">Aragon + Community Fund</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Pros</td>
      <td style="text-align:left">Manual / Personal approach & support</td>
      <td style="text-align:left">
        <p>Fast</p>
        <p>Small fees (~$10-$15)</p>
        <p>Extendable functionality</p>
        <p>Transparency by default</p>
        <p>Easy to setup a multisig</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Cons</td>
      <td style="text-align:left">
        <p>Costly ($10k - $150k)</p>
        <p>Can be Timely</p>
      </td>
      <td style="text-align:left">Some education needed</td>
    </tr>
  </tbody>
</table>Let’s review the tasks one by one.  


## Setup a secure wallet & Launch a token

With Aragon you can setup a multisig wallet. Connected to your other devices or you partners in order to preserve losing control over your tokens and funds. Each Aragon entity is coming with an ERC-20 compatible token that can be seen in wallets, put to exchange etc.  


![](https://lh6.googleusercontent.com/IKL3A79LBMpr9MkUMyKRkOTm2kPPfnSRgbVQhOo7dRrv6xTLEZrnx443Oi5_ygbHVvnv_mmOw6a92vpCqw_XWgMRuQ_L7d1VPavEaC1lFhODSp4YXf6NxE83fbSTqsnLcF3cOvlL)

Then from there, you can assign tokens to your presale investors, team, advisors and more.

## Mass distribute the token

For mass distribution, we’re now doing a product called “community fund” or Apiary. It’s an application that can be installed inside Aragon and allow the autosale with different pricing models, accepting different currencies, etc.

### Setup a pricing model

There’re such options:

* Linear with a single price per stage \(can be several stages\)
* Continuous token model

The linear is the most used model, where you assign a price for purchase.

But if you’re interested you can check continious model as well: [https://4ire-labs.gitbook.io/apiary/research/apiary-research-by-luke-duncan](https://4ire-labs.gitbook.io/apiary/research/apiary-research-by-luke-duncan)

### Payment methods etc

![](https://lh3.googleusercontent.com/M0yzsNwuvxa981kGcNND9nmR6vxknXlWc52FiUen0d5Xla4V_PIPwY01JLMPRAKsBTsWC5PV1jeMV7qRAVwlaD4xp79pl2TjmhCHwXClii4QOJJVdAguzBvAjpoPH7I-3Hup2_hq)

## How do we ensure security of the system? Was there any form of PEN \(penetration\) testing conducted on the dashboard application? Have you performed security audit by external firm? Can you show? <a id="ICONXCustomerFAQ-Howdoweensuresecurityofthesystem?WasthereanyformofPEN(penetration)testingconductedonthedashboardapplication?Haveyouperformedsecurityauditbyexternalfirm?Canyoushow?"></a>

There're a couple of potential attacks applied to ICOs:

* Smart contracts that manage funds – we use the contracts developed by OpenZeppelin and audited by the community. It's a gold standard for the crowdfunding smart contracts.
* The app itself – there're a couple of architecture design measures applied to not have a single point of failure. We also don't store the open keys to any wallets. The app is under monitoring and can sustain a high volume of traffic.
* Social engineering \(e.g. fake domains, direct messages in groups etc\) – we don't \(and can't\) protect from that, we can only support you with advice.

During the support period our engineers are ready to resolve any tech issues in the fast manner.

## What currencies are supported? <a id="ICONXCustomerFAQ-Whatcurrenciesaresupported?"></a>

Native support of Ethereum and Bitcoin \(we host their nodes\) and all altcoins available through the ShapeShift \([list](https://shapeshift.io/#/coins)\).

## How are exchange rates between BTC, ETH and other supported currencies being calculated? How often is the exchange rate adjusted? <a id="ICONXCustomerFAQ-HowareexchangeratesbetweenBTC,ETHandothersupportedcurrenciesbeingcalculated?Howoftenistheexchangerateadjusted?"></a>

We updated the rates from the Coinbase every 2 hours.

## Where are the funds stored during token sale? <a id="ICONXCustomerFAQ-Wherearethefundsstoredduringtokensale?"></a>

Ethereum funds are transferred straight to the ICO manager wallet. Bitcoin and altcoins \(exchanged to BTC during the purchase\) are stored on node with the possibility to withdraw to the ICO manager wallet at any time.

## Who has access to these private keys? <a id="ICONXCustomerFAQ-Whohasaccesstotheseprivatekeys?"></a>

The BTC private keys stored at the server, encrypted by the ICO manager password. So that only having this password transactions are possible.

## Which external KYC providers are integrated? <a id="ICONXCustomerFAQ-WhichexternalKYCprovidersareintegrated?"></a>

Onfido, Sum & Substance, Cynopsis

## Is your site GDPR compliant? <a id="ICONXCustomerFAQ-IsyoursiteGDPRcompliant?"></a>

Currently it lacks some points, though it should be ready by September.

## Do you make smart contract for token, as well as smart contract for crowd sale? <a id="ICONXCustomerFAQ-Doyoumakesmartcontractfortoken,aswellassmartcontractforcrowdsale?"></a>

Right

## When do buyers get their tokens? <a id="ICONXCustomerFAQ-Whendobuyersgettheirtokens?"></a>

It depends on the crowdsale settings: can be straight away or they can be frozen until end of ICO + x days.

## Will your developers support us during token sale? In case of attacks, will you help us? <a id="ICONXCustomerFAQ-Willyourdeveloperssupportusduringtokensale?Incaseofattacks,willyouhelpus?"></a>

Yes, we have a paid support during the stages of ICO.

## Where is your company and team based? <a id="ICONXCustomerFAQ-Whereisyourcompanyandteambased?"></a>

Kyiv, Ukraine

## What successful ICO have you done? What are you running currently <a id="ICONXCustomerFAQ-WhatsuccessfulICOhaveyoudone?Whatareyourunningcurrently"></a>

There're a couple we can't name due to NDA agreement, though [http://winstars.io/](http://winstars.io/) is one of the latest we can name.

## Please share username password for admin user functionality as well as investor <a id="ICONXCustomerFAQ-Pleaseshareusernamepasswordforadminuserfunctionalityaswellasinvestor"></a>

For the investor you can easily register or check [https://t.co/psMlXASiWE](https://t.co/psMlXASiWE)

For the admin panel – sorry, we can show it only on the call or maybe make a recording in some time. With the admin access it's easy to take service down. 

## Why the separate paid support is needed?

We guarantee the quality of the code, though it's only part of the working solution. The server and cryptonodes maintenance is something that needs constant attention.  As downtime in the crowdfunding campaigns can be quite costly we setup tools and allocate some time for that issues. Possible tasks that support is intended to solve:

* stop of the cryptonode,
* smart contract ran out of gas,
* abnormal server activity and possible attacks,
* helping the customer support to answer customer requests.

The work of the service without the support is theoretically possible, though will take much longed to research the problem \(instead of just fixing it\) and will move part of the tasks to the ICO manager \(e.g. checking the contracts, updating stages etc\).



