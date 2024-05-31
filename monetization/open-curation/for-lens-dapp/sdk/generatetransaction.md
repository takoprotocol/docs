# generateTransaction()

<table><thead><tr><th width="160">SDK</th><th>generateTransaction()</th></tr></thead><tbody><tr><td>Description</td><td>Generate transaction parameter to call the Tako Open Curation Contract</td></tr><tr><td>Nature</td><td>Method of Class</td></tr></tbody></table>

## Parameters

<table><thead><tr><th width="126">Name</th><th width="104">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>from</td><td>string</td><td>YES</td><td>The EVM-compatible wallet address of the user</td></tr><tr><td>abiData</td><td>string</td><td>YES</td><td>The calldata for calling the Tako Open Curation Contract</td></tr><tr><td>value</td><td>bigint</td><td>YES</td><td>Token amount</td></tr><tr><td>gasLimit</td><td>bigint</td><td>YES</td><td>Gas limit</td></tr></tbody></table>

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
const abiData = await lensOpenCuration.generateBidAbiData("0x47-0x01-DA-4649c8f1", "0x0000000000000000000000000000000000000000", amount);
const estimatedGas = await lensOpenCuration.estimateGas("0xaddress", takoHubInfo.contract, abiData, amount);
const transaction = await lensOpenCuration.generateTransaction("0xaddress", abiData, amount, estimatedGas * BigInt(3));
```
{% endcode %}

## Example Returns

```json
{
  to: '0xC158A4319BC125e315120DbDfBEa8b8343aa3234',
  value: 325n,
  gasLimit: 432513n,
  maxPriorityFeePerGas: BigNumber { _hex: '0x59682f00', _isBigNumber: true },
  maxFeePerGas: BigNumber { _hex: '0x59682f1e', _isBigNumber: true },
  nonce: 43,
  type: 2,
  chainId: 80001,
  data: '0x07de204500000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001450000000000000000000000000000000000000000000000000000000000000015307834372d307830312d44412d34363439633866310000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000000'
}
```
