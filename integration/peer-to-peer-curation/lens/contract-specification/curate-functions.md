# Curate Functions

## settings

Read the table below for more details

`function settings(address token, uint256 min, bool[] calldata disableAuditTypes) external`

<table><thead><tr><th width="214.33333333333331">Name</th><th width="142">Type</th><th>Description</th></tr></thead><tbody><tr><td>token</td><td>address</td><td>The accepted token address</td></tr><tr><td>min</td><td>uint256</td><td>The minimum accepted token amount</td></tr><tr><td>disableAuditTypes</td><td>bool[]</td><td>For the accepted BidType (including Post, Comment, Mirror), please fill in True or False in the order of Post, Comment, Mirror. For example, if Curator only accepts the Comment type of Bid, fill in [false, true, false]</td></tr></tbody></table>

## setMinBid

Read the table below for more details

`function setMinBid(address token, uint256 min) external`

<table><thead><tr><th width="155.33333333333331">Name</th><th width="143">Type</th><th>Description</th></tr></thead><tbody><tr><td>token</td><td>address</td><td>The accepted token address</td></tr><tr><td>min</td><td>uint256</td><td>The minimum accepted token amount</td></tr></tbody></table>

## setDisableAuditTypes

Read the table below for more details

`function setDisableAuditTypes(bool[] calldata disableAuditTypes) external`

<table><thead><tr><th width="210.33333333333331">Name</th><th width="142">Type</th><th>Description</th></tr></thead><tbody><tr><td>disableAuditTypes</td><td>bool[]</td><td>For the accepted BidType (including Post, Comment, Mirror), please fill in True or False in the order of Post, Comment, Mirror. For example, if Curator only accepts the Comment type of Bid, fill in [false, true, false]</td></tr></tbody></table>

## auditBidPost

Accept the bid, the curator will collect the token from the bid, and Tako will automatically send a publication on Lens for the curator

`function auditBidPost(uint256 index, uint256 curatorId, DataTypes.EIP712Signature calldata sig) external nonReentrant`

<table><thead><tr><th width="156.33333333333331">Name</th><th width="167">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr><tr><td>curatorId</td><td>uint256</td><td>The curator’s Lens profile id</td></tr><tr><td>sig</td><td>EIP712Signagure</td><td><a href="https://eips.ethereum.org/EIPS/eip-712">https://eips.ethereum.org/EIPS/eip-712</a></td></tr></tbody></table>

## auditBidMirror

Accept the bid, the curator will collect the token from the bid, and Tako will automatically send a publication on Lens for the curator

`function auditBidMirror(uint256 index, uint256 curatorId, DataTypes.EIP712Signature calldata sig) external nonReentrant`

<table><thead><tr><th width="149.33333333333331">Name</th><th width="165">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr><tr><td>curatorId</td><td>uint256</td><td>The curator’s Lens profile id</td></tr><tr><td>sig</td><td>EIP712Signagure</td><td><a href="https://eips.ethereum.org/EIPS/eip-712">https://eips.ethereum.org/EIPS/eip-712</a></td></tr></tbody></table>

## auditBidComment

Accept the bid, the curator will collect the token from the bid, and Tako will automatically send a publication on Lens for the curator

`function auditBidComment(uint256 index, uint256 curatorId, DataTypes.EIP712Signature calldata sig) external nonReentrant`

<table><thead><tr><th width="144.33333333333331">Name</th><th width="164">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr><tr><td>curatorId</td><td>uint256</td><td>The curator’s Lens profile id</td></tr><tr><td>sig</td><td>EIP712Signagure</td><td><a href="https://eips.ethereum.org/EIPS/eip-712">https://eips.ethereum.org/EIPS/eip-712</a></td></tr></tbody></table>

## loanWithSig

Momoka is now running for Lens. The user’s publications are possibly sent to the Momoka system or Polygon (the old mechanism).&#x20;

So part of the publications are from the Momoka, and the others are from the Polygon. The data on Momoka and Polygon is separate. So the users cannot comment or mirror using Polygon for the Momoka publications.&#x20;

Suppose the booster wants the curator to comment on or mirror a Momoka publication. The comment or mirror result will be sent to Momoka after the curator accepts the bid. Because Lens does not allow users to comment or mirror Momoka publications using Polygon.&#x20;

Tako will do all the curate works for curators, such as comment, mirror, etc. It will be straightforward if Tako does all the work using Polygon because they all happen in Polygon.&#x20;

But if Tako has to use Momoka, it won’t be easy because Momoka and Polygon are separate.&#x20;

So it would be best to do extra work to verify whether the curate works are done. Go to the API doc VerifyBid for more detail.&#x20;

The curator can claim his reward from the booster bid after verification.

This function is used to claim the reward.

<mark style="color:red;">Please use the API</mark> `verifyOpenCurationBid` <mark style="color:red;">to obtain the</mark> `sig` <mark style="color:red;">and</mark> `relayer` <mark style="color:red;">information.</mark>

`function loanWithSig(uint256 index, uint256 curatorId, address relayer, string calldata contentId, DataTypes.EIP712Signature calldata sig) external nonReentrant`

<table><thead><tr><th width="136.33333333333331">Name</th><th width="169">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr><tr><td>curatorId</td><td>uint256</td><td>The curator’s Lens profile id</td></tr><tr><td>relayer</td><td>address</td><td>An EVM-comptiable externally owned account, for signless feature</td></tr><tr><td>contentId</td><td>string</td><td>Tako will auto-submit a publication to Lens in post, comment, and mirror bids while the curator accepts the bid. The contentId is the publication Id on Lens</td></tr><tr><td>sig</td><td>EIP712Signature</td><td><a href="https://eips.ethereum.org/EIPS/eip-712">https://eips.ethereum.org/EIPS/eip-712</a></td></tr></tbody></table>
