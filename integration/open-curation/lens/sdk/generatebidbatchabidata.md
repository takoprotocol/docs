# generateBidBatchAbiData()

<table><thead><tr><th width="160">SDK</th><th>generateBidBatchAbiData()</th></tr></thead><tbody><tr><td>Description</td><td>Similar to generateBidAbiData(), supports batch operations.</td></tr><tr><td>Nature</td><td>Method of Class</td></tr></tbody></table>

## Parameters

<table><thead><tr><th width="153">Name</th><th width="104">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>contentIds</td><td>string[]</td><td>YES</td><td>The id of publication that is wating to be curated, such as 0x8d11-0x07-DA-1cdac4db</td></tr><tr><td>bidTokens</td><td>string[]</td><td>YES</td><td>The address of token. Default to 0x0000000000000000000000000000000000000000 , namely Matic</td></tr><tr><td>bidAmounts</td><td>bigint[]</td><td>YES</td><td>The amount of bidToken</td></tr><tr><td>merkleIndex</td><td>number</td><td>NO</td><td>(Ignore it on testnet)</td></tr><tr><td>merkleProof</td><td>string[]</td><td>NO</td><td>(Ignore it on testnet)</td></tr></tbody></table>

## Example Code

Refer to: [generatebidabidata.md](generatebidabidata.md "mention")
