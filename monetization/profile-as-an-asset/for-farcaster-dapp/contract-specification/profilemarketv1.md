# ProfileMarketV1

## setFeeDestination

Sets the destination address for protocol fees

`function setFeeDestination(address _feeDestination) external onlyOwner`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>_feeDestination</td><td>address</td><td>The address that receives the protocol fees</td></tr></tbody></table>

## setProtocolBuyFeePercent

Sets the buy fee percentage for the protocol

`function setProtocolBuyFeePercent(uint256 _feePercent) external onlyOwner`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>_feePercent</td><td>uint256</td><td>The fee percent. 0 - 100%</td></tr></tbody></table>

## setProtocolSellFeePercent

Sets the sell fee percentage for the protocol

`function setProtocolSellFeePercent(uint256 _feePercent) external onlyOwner`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>_feePercent</td><td>uint256</td><td>The fee percent. 0 - 100%</td></tr></tbody></table>

## setCreatorBuyFeePercent

Sets the buy fee percentage for the creator

`function setCreatorBuyFeePercent(uint256 _feePercent) external onlyOwner`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>_feePercent</td><td>uint256</td><td>The fee percent. 0 - 100%</td></tr></tbody></table>

## setCreatorSellFeePercent

Sets the sell fee percentage for the creator

`function setCreatorSellFeePercent(uint256 _feePercent) external onlyOwner`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>_feePercent</td><td>uint256</td><td>The fee percent. 0 - 100%</td></tr></tbody></table>

## setOpenInit

Opens oc closes the platform for shares issuance

`function setOpenInit(bool isOpen) external onlyOwner`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>isOpen</td><td>bool</td><td>true or false</td></tr></tbody></table>

## getBuyPrice

Retrieves the price for buying shares

`function getBuyPrice(uint256 creatorId, uint256 amount) external view`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>creatorId</td><td>uint256</td><td>The Farcaster ID of creator</td></tr><tr><td>amount</td><td>uint256</td><td>The amount of Key buys</td></tr></tbody></table>

## getSellPrice

Retrieves the price for selling shares

`function getSellPrice( uint256 creatorId, uint256 amount ) external view`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>creatorId</td><td>uint256</td><td>The Farcaster ID of creator</td></tr><tr><td>amount</td><td>uint256</td><td>The amount of Key sells</td></tr></tbody></table>

## createSharesForPiecewise

Allows a creator to issue shares with a piecewise pricing model

`function createSharesForPiecewise(uint256 creatorId, uint256 startPrice, uint256 initialSupply, uint256 totalSupply, uint256 a, uint256 b, bool signOfb, uint256 k, bool signOfk) public nonReentrant`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>creatorId</td><td>uint256</td><td>The Farcaster ID of creator</td></tr><tr><td>startPrice</td><td>uint256</td><td>The amount of Key sells</td></tr><tr><td>initialSupply</td><td>uint256</td><td></td></tr><tr><td>totalSupply</td><td>uint256</td><td></td></tr><tr><td>a</td><td>uint256</td><td></td></tr><tr><td>b</td><td>uint256</td><td></td></tr><tr><td>signOfb</td><td>bool</td><td></td></tr><tr><td>k</td><td>uint256</td><td></td></tr><tr><td>signOfk</td><td>bool</td><td></td></tr></tbody></table>

## buyShares

Allows a user to buy shares

`function buyShares(uint256 creatorId, uint256 sharesAmount) public payable nonReentrant()`

## sellShare

Allows a user to sell a single share

`function sellShare(uint256 tokenId, uint256 priceLimit) external nonReentrant`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>tokenId</td><td>uint256</td><td></td></tr><tr><td>priceLimit</td><td>uint256</td><td></td></tr></tbody></table>

## sellShares

Allows a user to sell multiple shares

`function sellShares(uint256[] memory tokenIds, uint256 priceLimit) external nonReentrant`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>tokenIds</td><td>uint256[]</td><td></td></tr><tr><td>priceLimit</td><td>uint256</td><td></td></tr></tbody></table>

## claim

Allows a user to claim accumulated fees

`function claim() external nonReentrant`

