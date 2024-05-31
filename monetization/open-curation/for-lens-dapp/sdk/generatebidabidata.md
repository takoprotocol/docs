# generateBidAbiData()

<table><thead><tr><th width="160">SDK</th><th>generateBidAbiData()</th></tr></thead><tbody><tr><td>Description</td><td>Generate calldata to call the Tako Open Curation Contract</td></tr><tr><td>Nature</td><td>Method of Class</td></tr></tbody></table>

## Parameters

<table><thead><tr><th width="153">Name</th><th width="104">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>contentId</td><td>string</td><td>YES</td><td>The id of publication that is wating to be curated, such as 0x8d11-0x07-DA-1cdac4db</td></tr><tr><td>bidToken</td><td>string</td><td>YES</td><td>The address of token. Default to 0x0000000000000000000000000000000000000000 , namely Matic</td></tr><tr><td>bidAmount</td><td>bigint</td><td>YES</td><td>The amount of bidToken</td></tr><tr><td>merkleIndex</td><td>number</td><td>NO</td><td>(Ignore it on testnet)</td></tr><tr><td>merkleProof</td><td>string[]</td><td>NO</td><td>(Ignore it on testnet)</td></tr></tbody></table>

## Example Code

{% code fullWidth="false" %}
```typescript
import { CONSTANT, TakoOpenCuration } from 'tako-open-curation'

const tako = new TakoOpenCuration(CONSTANT.Network.TESTNET)
const lensOpenCuration = tako.lensOpenCuration

const takoHubInfo = await lensOpenCuration.takoHubInfo();
const amount = BigInt(325); // 325 GWEI
const abiData = await lensOpenCuration.generateBidAbiData("0x47-0x01-DA-fece722d", "0x0000000000000000000000000000000000000000", amount);
```
{% endcode %}

## Example Returns

```json
0x07de204500000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001450000000000000000000000000000000000000000000000000000000000000015307834372d307830312d44412d66656365373232640000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000000
```
