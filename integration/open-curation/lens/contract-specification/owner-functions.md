# Owner Functions

## setFeeCollector

The administrator can collect the fee from every bid. When one bid is complete, the FeeCollect address will collect the fee, and the rest will be sent to the curator.

`function setFeeCollector( address newsFeeCollector, uint256 newFeeRate ) external onlyOwner`

<table><thead><tr><th width="198.33333333333331">Name</th><th width="113">Type</th><th>Description</th></tr></thead><tbody><tr><td>newsFeeCollector</td><td>address</td><td>An EVM-compatible address for collecting fees</td></tr><tr><td>newFeeRate</td><td>uint256</td><td>Fee rate charged after a bid is executed</td></tr></tbody></table>

## setGovernance

Set up administrator addresses

`function setGovernance(address gov, bool whitelist) external onlyOwner`

<table><thead><tr><th width="203.33333333333331">Name</th><th width="115">Type</th><th>Description</th></tr></thead><tbody><tr><td>gov</td><td>address</td><td>An EVM-compatible address</td></tr><tr><td>whitelist</td><td>bool</td><td>"true" means setting as an administrator<br>"false" means revoking administrator privileges</td></tr></tbody></table>
