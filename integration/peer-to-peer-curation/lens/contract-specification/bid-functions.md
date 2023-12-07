# Bid Functions

## bid

The creators hope more people can read their publications. So they need to boost their publications, and Tako provides the boost feature. The bidders(namely the creators) can send a bid to curators (such as a KOL in some fields), and there are three types of bids: Post, Comment, and Mirror. After accepting the Post bid, the curator should post a new publication on Lens. After accepting the Comment bid, the curator should comment on the creator's publication on Lens. After accepting the Mirror bid, the curator should mirror the creator's publication on Lens. Then more and more people will read your publication.

`function bid( BidData calldata vars, BidType bidType, DataTypes.MerkleVerifyData calldata verifyData ) external payable nonReentrant onlyWhitelisted(verifyData)`

<table><thead><tr><th width="160.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>vars</td><td>BidData</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>bidType</td><td>BidType</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>verifyData</td><td>MerkleVerifyData</td><td>Verify if the bid creator is on the whitelist<br>Go to the page “Enums and Functions” for more details</td></tr></tbody></table>

## bidBatch

Similar to bid, supports batch operations.

`function bidBatch(BidData[] calldata vars, BidType[] calldata bidType, DataTypes.MerkleVerifyData calldata verifyData) external payable nonReentrant onlyWhitelisted(verifyData)`

<table><thead><tr><th width="162.33333333333331">Name</th><th width="175">Type</th><th>Description</th></tr></thead><tbody><tr><td>vars</td><td>BidData[]</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>bidType</td><td>BidType[]</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>verifyData</td><td>MerkleVerifyData</td><td>Verify if the bid creator is on the whitelist<br>Go to the page “Enums and Functions” for more details</td></tr></tbody></table>

## bidMomoka

Similar to bid

Momoka is now running for Lens. The user’s publications are possibly sent to the Momoka system or Polygon (the old mechanism). So part of the publications are from the Momoka, and the others are from the Polygon. The data on Momoka and Polygon is separate. So the users cannot comment or mirror using Polygon for the Momoka publications. Suppose the bidder wants the curator to comment on or mirror a Momoka publication. The comment or mirror result will be sent to Momoka after the curator accepts the bid. Because Lens does not allow users to comment or mirror Momoka publications using Polygon

So please choose the function bid or the function bidMomoka according to the actual situation.

`function bidMomoka(MomokaBidData calldata vars, BidType bidType, DataTypes.MerkleVerifyData calldata verifyData) external payable nonReentrant onlyWhitelisted(verifyData)`

<table><thead><tr><th width="168.33333333333331">Name</th><th width="176">Type</th><th>Description</th></tr></thead><tbody><tr><td>vars</td><td>MomokaBidData</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>bidType</td><td>BidType</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>verifyData</td><td>MerkleVerifyData</td><td>Verify if the bid creator is on the whitelist<br>Go to the page “Enums and Functions” for more details</td></tr></tbody></table>

## bidMomokaBatch

Similar to bidMomoka, supports batch operations.

`function bidMomokaBatch(MomokaBidData[] calldata vars, BidType[] calldata bidType, DataTypes.MerkleVerifyData calldata verifyData) external payable nonReentrant onlyWhitelisted(verifyData)`

<table><thead><tr><th width="178.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>vars</td><td>MomokaBidData[]</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>bidType</td><td>BidType[]</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>verifyData</td><td>MerkleVerifyData</td><td>Verify if the bid creator is on the whitelist<br>Go to the page “Enums and Functions” for more details</td></tr></tbody></table>

## updateBid

Can only update duration and amount.

`function updateBid(uint256 index, uint256 duration, uint256 amount) external payable nonReentrant`

<table><thead><tr><th width="179.33333333333331">Name</th><th width="175">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr><tr><td>duration</td><td>uint256</td><td>The valid duration of the bid, a UNIX timestamp</td></tr><tr><td>amount</td><td>uint256</td><td>The amount of bid token</td></tr></tbody></table>

## updateBidMomoka

Can only update duration and amount.

`function updateBidMomoka(uint256 index, uint256 duration, uint256 amount) external payable nonReentrant`

<table><thead><tr><th width="186.33333333333331">Name</th><th width="174">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr><tr><td>duration</td><td>uint256</td><td>The valid duration of the bid, a UNIX timestamp</td></tr><tr><td>amount</td><td>uint256</td><td>The amount of bid token</td></tr></tbody></table>

## claimBackBid

Claim back the token after the bid expires

`function claimBackBid(uint256 index) external nonReentrant`

<table><thead><tr><th width="188.33333333333331">Name</th><th width="173">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr></tbody></table>

## claimBackBidBatch

Similar to bid, supports batch operations

`function claimBackBidBatch( uint256[] calldata indexArr ) external nonReentrant`

<table><thead><tr><th width="194.33333333333331">Name</th><th width="169">Type</th><th>Description</th></tr></thead><tbody><tr><td>indexArr</td><td>uint256[]</td><td>The indexes of bids</td></tr></tbody></table>

## claimBackBidMomoka

Claim back the token after the bid expires

`function claimBackBidMomoka(uint256 index) external nonReentrant`

<table><thead><tr><th width="188.33333333333331">Name</th><th width="173">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr></tbody></table>

## claimBackBidMomokaBatch

Similar to bid, supports batch operations

`function claimBackBidMomokaBatch( uint256[] calldata indexArr ) external nonReentrant`

<table><thead><tr><th width="194.33333333333331">Name</th><th width="169">Type</th><th>Description</th></tr></thead><tbody><tr><td>indexArr</td><td>uint256[]</td><td>The indexes of bids</td></tr></tbody></table>
