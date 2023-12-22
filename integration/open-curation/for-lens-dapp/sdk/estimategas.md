# estimateGas()

<table><thead><tr><th width="160">SDK</th><th>estimateGas()</th></tr></thead><tbody><tr><td>Description</td><td>Estimate the gas consumption for the transaction</td></tr><tr><td>Nature</td><td>Method of Class</td></tr></tbody></table>

## Parameters

<table><thead><tr><th width="101">Name</th><th width="104">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>from</td><td>string</td><td>YES</td><td>The EVM-compatible wallet address of the user</td></tr><tr><td>to</td><td>string</td><td>YES</td><td>The contract address of Tako Open Curation<br>(Use takoHubInfo() to retrieve the contract address)</td></tr><tr><td>data</td><td>string</td><td>YES</td><td>The calldata for calling the Tako Open Curation Contract</td></tr><tr><td>value</td><td>bigint</td><td>YES</td><td>Token amount</td></tr></tbody></table>

## Example Code

{% code fullWidth="false" %}
```typescript
import { ethers } from 'ethers'
import { CONSTANT, TakoOpenCuration } from 'tako-open-curation'

const tako = new TakoOpenCuration(CONSTANT.Network.TESTNET)
const lensOpenCuration = tako.lensOpenCuration
const apikey = "Your Alchemy API Key"
const web3Provider = new ethers.providers.AlchemyProvider(80001, apikey)
lensOpenCuration.provider = web3Provider

const takoHubInfo = await lensOpenCuration.takoHubInfo();
const amount = BigInt(325); // 325 GWEI
const abiData = await lensOpenCuration.generateBidAbiData("0x47-0x01-DA-fece722d", "0x0000000000000000000000000000000000000000", amount);
const estimatedGas = await lensOpenCuration.estimateGas("0xaddress", takoHubInfo.contract, abiData, amount);
```
{% endcode %}

## Example Returns

{% code overflow="wrap" %}
```json
// bigint
144171n
```
{% endcode %}
