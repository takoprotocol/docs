# Bid Functions

## bid

The creators hope more people can read their publications. So they need to boost their publications, and Tako provides the boost feature. The bidders(namely the creators) can send a bid to curators, such as a KOL, in some fields, and there are three types of bids: Casts, Reply, and Recasts. After accepting the Casts bid, the curator should cast a new publication on Farcaster. After accepting the Reply bid, the curator should reply to the creator's publication on Farcaster. After accepting the Recasts bid, the curator should recast the creator's publication on Farcaster. Then, more and more people will read your publication

`function bid( BidData calldata vars, BidType bidType, DataTypes.MerkleVerifyData calldata verifyData ) external payable nonReentrant onlyWhitelisted(verifyData)`

<table><thead><tr><th width="160.33333333333331">Name</th><th width="170">Type</th><th>Description</th></tr></thead><tbody><tr><td>vars</td><td>BidData</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>bidType</td><td>BidType</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>verifyData</td><td>MerkleVerifyData</td><td>Verify if the bid creator is in the whitelist<br>Go to the page “Enums and Functions” for more details</td></tr></tbody></table>

## bidBatch

Similar to bid, supports batch operations

`function bidBatch(BidData[] calldata vars, BidType[] calldata bidType, DataTypes.MerkleVerifyData calldata verifyData) external payable nonReentrant onlyWhitelisted(verifyData)`

<table><thead><tr><th width="162.33333333333331">Name</th><th width="180">Type</th><th>Description</th></tr></thead><tbody><tr><td>vars</td><td>BidData[]</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>bidType</td><td>BidType[]</td><td>Go to the page “Enums and Functions” for more details</td></tr><tr><td>verifyData</td><td>MerkleVerifyData</td><td>Verify if the bid creator is in the whitelist<br>Go to the page “Enums and Functions” for more details</td></tr></tbody></table>

## updateBid

Can only update duration and amount

`function updateBid(uint256 index, uint256 duration, uint256 amount) external payable nonReentrant`

<table><thead><tr><th width="179.33333333333331">Name</th><th width="175">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr><tr><td>duration</td><td>uint256</td><td>The valid duration of the bid, a UNIX timestamp</td></tr><tr><td>amount</td><td>uint256</td><td>The amount of bid token</td></tr><tr><td>verifyData</td><td>MerkleVerifyData</td><td>Verify if the bid creator is in the whitelist<br>Go to the page “Enums and Functions” for more details</td></tr></tbody></table>

## claimBackBid

Claim back the token after the bid expires

`function claimBackBid(uint256 index) external nonReentrant`

<table><thead><tr><th width="188.33333333333331">Name</th><th width="173">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of bid</td></tr></tbody></table>

## claimBackBidBatch

Similar to bid, supports batch operations

`function claimBackBidBatch( uint256[] calldata indexArr ) external nonReentrant`

<table><thead><tr><th width="194.33333333333331">Name</th><th width="169">Type</th><th>Description</th></tr></thead><tbody><tr><td>indexArr</td><td>uint256[]</td><td>The indexes of bids</td></tr></tbody></table>

