# Bid Functions

## bid

After the Bid is posted, anyone can accept the Bid and complete the curation. After a certain period of time, the curation effectiveness is calculated, and the Curator with the best effectiveness can claim the reward. In Open Curation, the curation method is fixed as Quote Post. The curation effectiveness is calculated by summing the number of comments and mirrors received by the Curator's Quote Post.

`function bid( BidData calldata vars, DataTypes.MerkleVerifyData calldata verifyData ) external payable nonReentrant onlyWhitelisted(verifyData)`

<table><thead><tr><th width="160.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>vars</td><td>BidData</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>verifyData</td><td>MerkleVerifyData</td><td>Verify if the bid creator is on the whitelist<br>Go to the page “Enums and Functions” for more details</td></tr></tbody></table>

## bidBatch

Similar to bid, supports batch operations.

`function bidBatch( BidData[] calldata vars, DataTypes.MerkleVerifyData calldata verifyData ) external payable nonReentrant onlyWhitelisted(verifyData)`

<table><thead><tr><th width="162.33333333333331">Name</th><th width="175">Type</th><th>Description</th></tr></thead><tbody><tr><td>vars</td><td>BidData[]</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>verifyData</td><td>MerkleVerifyData</td><td>Verify if the bid creator is on the whitelist<br>Go to the page “Enums and Functions” for more details</td></tr></tbody></table>

## updateBid

`function updateBid( uint256 index, uint256 amount ) external payable nonReentrant`

<table><thead><tr><th width="162.33333333333331">Name</th><th width="175">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr><tr><td>amount</td><td>uint256</td><td>The amount of bid token</td></tr></tbody></table>

## claimBackBid

Claim back the token after the bid expires

`function claimBackBid(uint256 index) external nonReentrant`

<table><thead><tr><th width="188.33333333333331">Name</th><th width="173">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr></tbody></table>

## claimBackBidBatch

Similar to bid, supports batch operations

`function claimBackBidBatch( uint256[] calldata indexArr ) external nonReentrant`

<table><thead><tr><th width="194.33333333333331">Name</th><th width="169">Type</th><th>Description</th></tr></thead><tbody><tr><td>indexArr</td><td>uint256[]</td><td>The indexes of bids</td></tr></tbody></table>
