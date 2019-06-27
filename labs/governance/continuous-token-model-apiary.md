# Funding Public Goods

## Use Cases

* Open source software ecosystems
* News media
* Research

### Open Source Ecosystems \(e.g. Aragon Nest\)

This is the case where we’d like to do an efficient distribution of several funds and investors to a distributed network. If it’s impractical to deal with a analog registered company and the funds are allocated for a long term, we need a mechanism for keeping the initiatives live and sustainable. So somebody can initialise a purpose-driven initiative \(e.g. develop open-source software or maintain the Ethereum documentation\) and open funds allocation for the cause.

The initiator in such case may be not the person in charge or most responsible — his role is to describe the need and allow the crowdfunding. As the funds start to concentrate on such DAO account it can attract the executors to step in and do the work.

* [https://opencollective.com/](https://opencollective.com/)

### Creators Organization \(e.g. Patreon\)

[Patreon](http://www.patreon.com/) is a highly successful service for supporting the creators with $12M monthly payouts for over 100k or creators. With that Patreon has some issues with [censorship](http://www.openlettertopatreon.com/) and [high pledge fees](https://www.reddit.com/r/patreon/comments/7i8pwa/new_pledge_fee_discussion/). Not saying that it’s easily solved, though there’s a place for similar services, like [Stake Tree](https://staketree.com/). So a potential organization with more than 1 creator can do a responsible crowdfunding. It can be a podcast, youtube show, book, research etc.

* [https://www.ryhope.network/](https://www.ryhope.network/)
* knowledge repo DAOs

### Communities Public Projects \(e.g. game communities\)

Finally the existent communities can understand a need for some of the work needed, e.g. game communities. There could be a request for a community management, pr & growth or something like championship organization.

So the initiator can open up a DAO for maintaining the community and start crowdfunding. And if in any case the leaders are left the work is undertaken by newcomers or it’s liquidated.

* [https://www.spacehive.com/](https://www.spacehive.com/)

## Development Plan

### 0.1 Create crowdfunding smart contracts in Aragon

#### Fundraising app

The task is done in the new Fundraising app.

[![Fundraising &#x2013;&#xA0;Empty State](https://github.com/MaxSemenchuk/Apiary/raw/master/.gitbook/assets/webapp-1366px-fundraising-empty-state.jpg)](https://github.com/MaxSemenchuk/Apiary/blob/master/.gitbook/assets/webapp-1366px-fundraising-empty-state.jpg)

#### Creation of a fundraising campaign

[![Adding a new raising campaign](https://github.com/MaxSemenchuk/Apiary/raw/master/.gitbook/assets/webapp-1366px-fundraising-new-raise-2x-5.jpg)](https://github.com/MaxSemenchuk/Apiary/blob/master/.gitbook/assets/webapp-1366px-fundraising-new-raise-2x-5.jpg)

Terms: simplest option, public with stable price. In the initial version min is tight to 0, so there's no return. After expiration of the deadline all collected funds go directly to the org account \(before we implement the tap\).

Campaign name e.g. "Round 1".

Price and Min/Max caps are set in Ethereum. We set no minimum target to avoid the returns \(for now\).

[![List of Fundraising Campaigns](https://github.com/MaxSemenchuk/Apiary/raw/master/.gitbook/assets/webapp-1366px-fundraising-2x-1.jpg)](https://github.com/MaxSemenchuk/Apiary/blob/master/.gitbook/assets/webapp-1366px-fundraising-2x-1.jpg)

If we click on a campaign we can see details of the campaign.

[![Campaign Details](https://github.com/MaxSemenchuk/Apiary/raw/master/.gitbook/assets/webapp-1366px-fundraising-preview-2.jpg)](https://github.com/MaxSemenchuk/Apiary/blob/master/.gitbook/assets/webapp-1366px-fundraising-preview-2.jpg)



{% embed url="https://www.youtube.com/watch?v=MvS4YjsSTJQ&t=4s" %}

#### Important links:

* [Aragon Nest Proposal](https://github.com/aragon/nest/issues/78)
* [Aragon Funds Request](https://github.com/aragon/nest/pull/88)
* [Roadmap and Specifications](https://4ire-labs.gitbook.io/apiary/~/edit/drafts/-LLsqqwMXpIlqN0oyNiF/development-plan)
* [Demo](https://www.youtube.com/watch?v=MvS4YjsSTJQ)
* [Design in Figma](https://www.figma.com/file/ZqJYCbSyejYkVvlRfY81qQ/Apiary?node-id=0%3A1)

#### Join the conversation

* [Aragon Research forum thread](https://research.aragon.org/t/request-for-comment-aragon-crowdfunding-app-to-enable-more-responsible-crowdfunding-with-daos/144)
* [Telegram chat](https://t.me/joinchat/E9cyAxB_6FdwNvJ7Mh7wDQ)



1Hive's Apiary is a platform for emergent organization built on Aragon. Contributors stake tokens into organizations on the Apiary platform using a bonding curve. Funds held in the bonding curve's reserve pool are released over time into a discretionary pool that the Aragon DAO can use to reward contributors. Splitting funds into reserve and discretionary pools provides smart-contract enforced accountability between project contributors and patrons throughout the lifecycle of a project while simultaneously ensuring sufficient liquidity to support the emergence of a long-tail of micro-organizations.

## Possible Attacks

[https://blog.relevant.community/how-to-make-bonding-curves-for-continuous-token-models-3784653f8b17?gi=f275a521fc3b](https://blog.relevant.community/how-to-make-bonding-curves-for-continuous-token-models-3784653f8b17?gi=f275a521fc3b)

### Extraction of funds via bribing

Possible solution: priority in liquidation to voters who haven't supported extraction?

small continuous selling, buying only against the curve [https://medium.com/@mrdavey/dynamic-token-bonding-curves-41d36e43befa](https://medium.com/@mrdavey/dynamic-token-bonding-curves-41d36e43befa)

### Bonding curve exploit / race conditions

Solutions:

* Static bonding curve

