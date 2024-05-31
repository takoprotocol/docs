# FarcasterKey

## creatorIdOf

Get the creatorId by token ID

`function creatorIdOf(uint256 tokenId) external view`

<table><thead><tr><th width="160.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>tokenId</td><td>uint256</td><td>the ID of NFT token</td></tr></tbody></table>

## creatorIdsOf

Similar to creatorIdOf(), supports batch operations

`function creatorIdsOf(uint256[] calldata tokenIds) external view`

<table><thead><tr><th width="160.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>tokenId</td><td>uint256</td><td>the ID of NFT token</td></tr></tbody></table>

## creatorIdsOfOwner

Get the creatorIds by owner address

`function creatorIdsOfOwner(address tokenOwner) external view`

<table><thead><tr><th width="160.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>tokenOwner</td><td>address</td><td>the owner's address</td></tr></tbody></table>

## Mint

Mint the Profile Key NFT

`function mint(address to, uint256 amount, uint256 creatorId) external onlyFarcasterKeys`

<table><thead><tr><th width="160.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>to</td><td>address</td><td>The address that receives the NFTs</td></tr><tr><td>amount</td><td>uint256</td><td>The amount of Minted NFTs</td></tr><tr><td>creatorId</td><td>uint256</td><td>The creator's Farcaster ID</td></tr></tbody></table>

## Burn

Burn the profile Key NFT

`function burn(uint256 tokenId) external onlyFarcasterKeys`

<table><thead><tr><th width="160.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>tokenId</td><td>uint256</td><td>the ID of the profile key NFT</td></tr></tbody></table>

## totalMinted

Get the amount of minted NFTs

`function totalMinted() external view`

## totalBurned

Get the amount of burned NFTs

`function totalBurned() external view`

## setBaseURI

Set the base image URI of NFT

`function setBaseURI(string memory newBasURI) external onlyOwner`

<table><thead><tr><th width="160.33333333333331">Name</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>newBasURI</code></td><td>string</td><td>The image URI</td></tr></tbody></table>
