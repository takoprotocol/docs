# Peer-to-Peer Curation

The integration of this peer-to-peer curation module into a dApp allows users to boost the visibility of their content. They can offer curation bids on targeted profiles whose followers they seek to engage.

It could be a sufficiently inclusivized recommendation/advertisement solution as an effective alternative to the traditional centralized, algorithm-based, platform-curated solutions. Sharing content through these value-matching curations also enhances the engagement of diverse content within an ecosystem. This allows niche yet valuable content and their creators to be easily discovered. It also offers improved monetization opportunities for content creators, allowing them to leverage their social influence.

Basically, there are two roles in this peer-to-peer curation module: Bidder and Curator:

#### Bidder

Login with a wallet address or creator profile (e.g. Lens handle). They can:

* Create a bid: set up a curation bid by specifying the curation type, target Curator, bid amount, and bid duration. Curation types can include share (mirror in Lens protocol), comment, post, or quote post.
* Update a bid: modify the bid data before a bid expires, including extending durations or increasing bid amounts.&#x20;
* Cancel a bid (Claim back): reclaim funds from the smart contract if a bid expires or the curator has accepted but didn't claim the funds within 7 days.

#### Curator

Login with a creator profile (e.g. Lens handle). They can:

* Audit a bid: decide on a status change, i.e., whether to recommend it, to a received curation bid by evaluating the content and the bid amount.
* Claim: claim the funds after accepting and executing a curation.
* Set a minimum bid: set the minimum bid amount the Curator wants to receive.
* Set disabled audit types: specify the curation types that the Curator does not want to receive.

***

#### Supported Ecosystems

{% content-ref url="lens/" %}
[lens](lens/)
{% endcontent-ref %}

{% content-ref url="farcaster/" %}
[farcaster](farcaster/)
{% endcontent-ref %}
