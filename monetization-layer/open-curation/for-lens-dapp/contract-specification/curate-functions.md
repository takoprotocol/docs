# Curate Functions

## loanWithSig

You should do extra work to verify whether the curate works are done. Go to the API doc VerifyBid for more details

The curator can claim his reward from the booster bid after verification

This function is used to claim the reward

<mark style="color:red;">Please use the API</mark> `verifyOpenCurationBid` <mark style="color:red;">to obtain the</mark> `sig` <mark style="color:red;">and</mark> `relayer` <mark style="color:red;">information.</mark>

`function loanWithSig( uint256 index, uint256 curatorId, address relayer, string calldata contentId, DataTypes.EIP712Signature calldata sig ) external nonReentrant`

<table><thead><tr><th width="136.33333333333331">Name</th><th width="169">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr><tr><td>curatorId</td><td>uint256</td><td>The curator’s Lens profile id</td></tr><tr><td>relayer</td><td>address</td><td>An EVM-comptiable externally owned account, for signless feature</td></tr><tr><td>contentId</td><td>string</td><td>Tako will auto-submit a publication to Farcaster in cast, reply, and recast bids while the curator accepts the bid. The contentId is the publication Id on Farcaster</td></tr><tr><td>sig</td><td>EIP712Signature</td><td><a href="https://eips.ethereum.org/EIPS/eip-712">https://eips.ethereum.org/EIPS/eip-712</a></td></tr></tbody></table>

## loanWithRelayer

The winning curator needs to manually claim the reward using `loanWithSig`, but this function can help curators settle automatically.

The relayer will send the reward to the curator, eliminating the need for manual claiming. Curators only need to wait for the result after completing the curation. If they are ultimately winning, developers can call this function on your server, then they will receive the reward automatically.

`function loanWithRelayer( uint256 index, uint256 curatorId, address to, string calldata contentId ) external nonReentrant`

<table><thead><tr><th width="136.33333333333331">Name</th><th width="169">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr><tr><td>curatorId</td><td>uint256</td><td>The curator’s Lens profile id</td></tr><tr><td>relayer</td><td>address</td><td>An EVM-comptiable externally owned account, for signless feature</td></tr><tr><td>contentId</td><td>string</td><td>Tako will auto-submit a publication to Farcaster in cast, reply, and recast bids while the curator accepts the bid. The contentId is the publication Id on Farcaster</td></tr></tbody></table>

## loanBatchWithRelayer

Similar to loanWithRelayer, supports batch operations.

`function loanWithRelayer( uint256 index, uint256 curatorId, address to, string calldata contentId ) external nonReentrant`

<table><thead><tr><th width="136.33333333333331">Name</th><th width="169">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256[]</td><td>The index of bid</td></tr><tr><td>curatorId</td><td>uint256[]</td><td>The curator’s Lens profile id</td></tr><tr><td>relayer</td><td>address[]</td><td>An EVM-comptiable externally owned account, for signless feature</td></tr><tr><td>contentId</td><td>string[]</td><td>Tako will auto-submit a publication to Farcaster in cast, reply, and recast bids while the curator accepts the bid. The contentId is the publication Id on Farcaster</td></tr></tbody></table>
