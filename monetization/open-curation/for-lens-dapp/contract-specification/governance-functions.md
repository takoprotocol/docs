# Governance Functions

## setLensContracts

Set LensHub address and collectModule address. Read the Lens docs for more details. [https://docs.lens.xyz/docs/deployed-contract-addresses](https://docs.lens.xyz/docs/deployed-contract-addresses)

`function setLensContracts( address hub, address collectModule ) external onlyGov`

<table><thead><tr><th width="213.33333333333331">Name</th><th width="107">Type</th><th>Description</th></tr></thead><tbody><tr><td>hub</td><td>address</td><td>The contract address of LensHub</td></tr><tr><td>collectModule</td><td>address</td><td>The contract address of CollectMudule</td></tr></tbody></table>

## setMerkleRoot

Set up a Merkle Root Hash to verify the usage privilege of the address used for accessing Tako

`function setMerkleRoot(bytes32 newMerkleRoot) external onlyGov`

<table><thead><tr><th width="213.33333333333331">Name</th><th width="134">Type</th><th>Description</th></tr></thead><tbody><tr><td>newMerkleRoot</td><td>bytes32</td><td>A new merkle root</td></tr></tbody></table>

## whitelistBidToken

Set a whitelist of token types that can be used in transactions

`function whitelistBidToken(address token, bool whitelist) external onlyGov`

<table><thead><tr><th width="213.33333333333331">Name</th><th width="107">Type</th><th>Description</th></tr></thead><tbody><tr><td>token</td><td>address</td><td>The contract address of token</td></tr><tr><td>whitelist</td><td>bool</td><td>"true" represents adding to the whitelist, while "false" represents removing from the whitelist.</td></tr></tbody></table>

## whitelistRelayer

`function whitelistRelayer(address relayer, bool whitelist) external onlyGov`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="105">Type</th><th>Description</th></tr></thead><tbody><tr><td>relayer</td><td>address</td><td>The address of relayer</td></tr><tr><td>whitelist</td><td>bool</td><td>"true" represents adding to the whitelist<br>"false" represents removing from the whitelist.</td></tr></tbody></table>

## setCurateDuration

`function setCurateDuration(uint256 duration) external onlyGov`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="105">Type</th><th>Description</th></tr></thead><tbody><tr><td>duration</td><td>uint256</td><td>The period after the Bid is posted is referred to as CurateDuration. During this period, Curators accept the Bid, and upon completing the curation, the system records and tracks the curation's effectiveness. After the CurateDuration period, the Curator with the best curation effectiveness can claim the reward.</td></tr></tbody></table>

## setRewardClaimProtectionDuration

`function setRewardClaimProtectionDuration(uint256 duration) external onlyGov`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="105">Type</th><th>Description</th></tr></thead><tbody><tr><td>duration</td><td>uint256</td><td>After CurateDuration, the Bid concludes and enters a reward claim protection period called RewardClaimProtectionDuration. During this period, only the winning Curator can claim the reward. After the protection period expires, if the Curator has not claimed the reward, the Bidder can withdraw the reward.</td></tr></tbody></table>
