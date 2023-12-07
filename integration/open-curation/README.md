# Open Curation

The open curation module operates as a permissionless approach to content promotion, focusing on incentivizing real human engagement. It distinguishes itself from traditional methods by utilizing the Lens quote post function to monitor and record interactions, avoiding reliance on centralized and opaque algorithms.&#x20;

Within this permissionless module, anyone can participate in sharing a piece of content by quote posting. The reward offered by the content creator is granted to the curator who achieves the highest level of engagement on their quote post. This approach ensures that creators can maximize the value of their investment, while fans can actively support their favorite creators through their content and social influence.

The open curation module involves two primary roles:

#### Bidder

Login with a wallet address or creator profile (i.e. Lens handle). They can:

* Create a bid: set up an open curation bid by selecting a post and specifying the bid amount. The curation type is limited to quote posts, ensuring trustless settlement.
* Update a bid: modify the bid data before a bid expires, including extending durations or increasing bid amounts.
* Cancel a bid (Claim back): reclaim funds from the smart contract if a bid expires or the curator has accepted but didn't claim the funds within 7 days.

#### Curator

Login with a creator profile (i.e. Lens handle). They can:

* Curate: quote post an active open curation post through the Tako API
* Claim: after a specified period (T=48h), the sum of mirrors and comments on each quote post made through Tako's open curation module is calculated based on traceable and trustless data. The curator who created the quote post with the highest mirrors + comments can claim the reward.

***

#### Supported Ecosystems

{% content-ref url="lens/" %}
[lens](lens/)
{% endcontent-ref %}
