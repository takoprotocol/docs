# Governance Functions

## setMerkleRoot

Set up a Merkle Root Hash to verify the usage privilege of the address used for accessing Tako

`function setMerkleRoot(bytes32 newMerkleRoot) external onlyGov`

<table><thead><tr><th width="213.33333333333331">Name</th><th width="134">Type</th><th>Description</th></tr></thead><tbody><tr><td>newMerkleRoot</td><td>bytes32</td><td>A new merkle root</td></tr></tbody></table>

## whitelistBidToken

Set a whitelist of token types that can be used in transactions

`function whitelistBidToken(address token, bool whitelist) external onlyGov`

<table><thead><tr><th width="213.33333333333331">Name</th><th width="107">Type</th><th>Description</th></tr></thead><tbody><tr><td>token</td><td>address</td><td>The contract address of token</td></tr><tr><td>whitelist</td><td>bool</td><td>"true" represents adding to the whitelist<br>"false" represents removing from the whitelist.</td></tr></tbody></table>

## whitelistRelayer

`function whitelistRelayer(address relayer, bool whitelist) external onlyGov`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="105">Type</th><th>Description</th></tr></thead><tbody><tr><td>relayer</td><td>address</td><td>The address of relayer</td></tr><tr><td>whitelist</td><td>bool</td><td>"true" represents adding to the whitelist, while "false" represents removing from the whitelist.</td></tr></tbody></table>

## setToCuratorLimit

The bid can be sent to multiple curators at one time, and this function can limit the number of curators.

`function setToCuratorLimit(uint8 counter) external onlyGov`

<table><thead><tr><th width="200.33333333333331">Name</th><th width="117">Type</th><th>Description</th></tr></thead><tbody><tr><td>counter</td><td>uint8</td><td>Maximum number of target curators</td></tr></tbody></table>

## setMaxDuration

Bids can be set with a valid duration, and this method can restrict the maximum valid time

`function setMaxDuration(uint256 max) external onlyGov`

<table><thead><tr><th width="203.33333333333331">Name</th><th width="115">Type</th><th>Description</th></tr></thead><tbody><tr><td>max</td><td>uint256</td><td>Maximum valid duration for a bid</td></tr></tbody></table>
