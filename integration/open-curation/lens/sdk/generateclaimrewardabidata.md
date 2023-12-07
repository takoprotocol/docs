# generateClaimRewardAbiData()

<table><thead><tr><th width="160">SDK</th><th>verifyBid()</th></tr></thead><tbody><tr><td>Description</td><td><p>Generate calldata to call loanWithSig on Tako Open Curation Contarct<br>The curator can claim his reward from the booster bid after verification</p><p>This function is used to claim the reward</p></td></tr><tr><td>Nature</td><td>Method of Class</td></tr></tbody></table>

## Parameters

<table><thead><tr><th width="136.33333333333331">Name</th><th width="169">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>number</td><td>The index of bid</td></tr><tr><td>curatorId</td><td>number</td><td>The curator’s Lens profile id</td></tr><tr><td>relayer</td><td>string</td><td>An EVM-comptiable externally owned account, for signless feature</td></tr><tr><td>contentId</td><td>string</td><td>Tako will auto-submit a publication to Farcaster in cast, reply, and recast bids while the curator accepts the bid. The contentId is the publication Id on Farcaster</td></tr><tr><td>sig</td><td><p>object<br><br>{</p><p>  r: string,</p><p>  s: string,</p><p>  v: number,</p><p>  deadline: number</p><p>}</p></td><td><a href="https://eips.ethereum.org/EIPS/eip-712">https://eips.ethereum.org/EIPS/eip-712</a></td></tr></tbody></table>

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

const profileId = 189
const bidIndex = 27
const contentId = '0xbd-0x01-DA-a8a8cbd5'
const sig = await lensOpenCuration.verifyBid('0xaddress', bidIndex, contentId)
const abiData = await lensOpenCuration.generateClaimRewardAbiData(bidIndex, profileId, sig.relayer, contentId, sig.signature);
```
{% endcode %}

## Example Returns

```json
0xfa2fd476000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000000000bd000000000000000000000000197309df1f580884b5a2a75dfd842a524fd8ac150000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000001beb98124c99d8b8341464c7519cf97bf9c7cfe06485a6dd9bdfcdfe7aec42ab523e5c21579c58377166c65a2342a3181642d3e6d8ed5bd990517be5e719da77510000000000000000000000000000000000000000000000000000000065693fbb0000000000000000000000000000000000000000000000000000000000000015307862642d307830312d44412d61386138636264350000000000000000000000
```
