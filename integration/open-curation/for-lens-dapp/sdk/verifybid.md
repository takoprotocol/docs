# verifyBid()

<table><thead><tr><th width="160">SDK</th><th>verifyBid()</th></tr></thead><tbody><tr><td>Description</td><td>Verify if the curator's task is completed and the curation has the best effect. The evaluation criteria for the effect are the highest sum of mirror and comment quantities in the curation quotes.</td></tr><tr><td>Nature</td><td>Method of Class</td></tr></tbody></table>

## Parameters

<table><thead><tr><th width="168">Name</th><th width="111">Type</th><th width="121">Required</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>string</td><td>YES</td><td>The curator’s EVM-compatible address</td></tr><tr><td>index</td><td>number</td><td>NO</td><td>The index of bid</td></tr><tr><td>pubId</td><td>string</td><td>YES</td><td>The id of Quote publication created by the curator</td></tr></tbody></table>

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

const result2 = await lensOpenCuration.verifyBid('0xaddress', 27, '0xbd-0x01-DA-a8a8cbd5')
```
{% endcode %}

## Example Returns

```json
{
  chainId: 80001,
  contract: '0xC158A4319BC125e315120DbDfBEa8b8343aa3234',
  curateDuration: 700,
  relayer: '0x197309df1f580884B5A2A75DFd842a524Fd8AC15',
  signature: {
    r: '0x6a64291997eeb5630662cf07c380299e64850e1aab016387a6f36a7d995a8c42',
    s: '0x41f4198eae0bfe99a5dcb523b2d5807326146ddf54c198524eb277b954eab7b0',
    v: 28,
    deadline: 1701395889
  }
}
```
