# Contract Specification

## Contract File

TakoFarcasterHub.sol

## Overview

Create and receive bids using publications submitted on Farcaster.

If you deployed the contract independently, you can use the Admin Functions to initialize the properties for bid.

Create Bid Steps (use Bid Functions):

1. Choose the publication that you want it to be curated.
2. Compose bid data that match the contract's specifications, such as the target publication, curator's profile ID, bid price, etc.
3. Send your bid transaction.

Use the Curate Functions to claim the reward for curators.

Use the View Functions to view the data for bid.

Github: [https://github.com/takoprotocol/contracts](https://github.com/takoprotocol/contracts)

## Specification

{% content-ref url="enums-and-structs.md" %}
[enums-and-structs.md](enums-and-structs.md)
{% endcontent-ref %}

{% content-ref url="owner-functions.md" %}
[owner-functions.md](owner-functions.md)
{% endcontent-ref %}

{% content-ref url="governance-functions.md" %}
[governance-functions.md](governance-functions.md)
{% endcontent-ref %}

{% content-ref url="bid-functions.md" %}
[bid-functions.md](bid-functions.md)
{% endcontent-ref %}

{% content-ref url="curate-functions.md" %}
[curate-functions.md](curate-functions.md)
{% endcontent-ref %}

{% content-ref url="view-functions.md" %}
[view-functions.md](view-functions.md)
{% endcontent-ref %}
