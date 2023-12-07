# Curate Functions

## settings

Read the table below for more detail.

`function settings(address token, uint256 min, bool[] calldata disableAuditTypes) external`

<table><thead><tr><th width="214.33333333333331">Name</th><th width="142">Type</th><th>Description</th></tr></thead><tbody><tr><td>token</td><td>address</td><td>The accepted token address</td></tr><tr><td>min</td><td>uint256</td><td>The minimum accepted token amount</td></tr><tr><td>disableAuditTypes</td><td>bool[]</td><td>For the accepted BidType (including Casts, Reply, Recasts), please fill in True or False in the order of Casts, Reply, Recasts.<br>For example, if Curator only accepts the Reply type of Bid, fill in [false, true, false]</td></tr></tbody></table>

## setMinBid

Read the table below for more detail.

`function setMinBid(address token, uint256 min) external`

<table><thead><tr><th width="155.33333333333331">Name</th><th width="143">Type</th><th>Description</th></tr></thead><tbody><tr><td>token</td><td>address</td><td>The accepted token address</td></tr><tr><td>min</td><td>uint256</td><td>The minimum accepted token amount</td></tr></tbody></table>

## setDisableAuditTypes

Read the table below for more detail.

`function setDisableAuditTypes(bool[] calldata disableAuditTypes) external`

<table><thead><tr><th width="210.33333333333331">Name</th><th width="142">Type</th><th>Description</th></tr></thead><tbody><tr><td>disableAuditTypes</td><td>bool[]</td><td>For the accepted BidType (including Casts, Reply, Recasts), please fill in True or False in the order of Cast, Reply, Recast. For example, if Curator only accepts the Reply type of Bid, fill in [false, true, false]</td></tr></tbody></table>

## loanWithSig

It would be best to do extra work to verify whether the curate works are done. Go to the API doc VerifyBid for more details&#x20;

The curator can claim his reward from the booster bid after verification

This function is used to claim the reward

<mark style="color:red;">Please use the API</mark> `verifyOpenCurationBid` <mark style="color:red;">to obtain the</mark> `sig` <mark style="color:red;">and</mark> `relayer` <mark style="color:red;">information.</mark>

`function loanWithSig(uint256 index, uint256 curatorId, address relayer, string calldata contentId, DataTypes.EIP712Signature calldata sig) external`

<table><thead><tr><th width="136.33333333333331">Name</th><th width="169">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr><tr><td>curatorId</td><td>uint256</td><td>The curator’s FID</td></tr><tr><td>relayer</td><td>address</td><td>An EVM-comptiable externally owned account, for signless feature</td></tr><tr><td>contentId</td><td>string</td><td>Tako will auto-submit a publication to Farcaster in cast, reply, and recast bids while the curator accepts the bid. The contentId is the publication Id on Farcaster</td></tr><tr><td>sig</td><td>EIP712Signature</td><td><a href="https://eips.ethereum.org/EIPS/eip-712">https://eips.ethereum.org/EIPS/eip-712</a></td></tr></tbody></table>
