# register()

<table><thead><tr><th width="160">SDK</th><th>register()</th></tr></thead><tbody><tr><td>Description</td><td>After the curators complete the curation(i.e., quote the target publication on Lens), they must bind the Quoted Publication Id and Bid Index.<br>So that Tako can verify that the curators have completed the curation task.<br>This method is used to perform the binding.</td></tr><tr><td>Nature</td><td>Method of Class</td></tr></tbody></table>

## Parameters

<table><thead><tr><th width="124">Name</th><th width="101">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>number</td><td>YES</td><td>The index of bid</td></tr><tr><td>pubId</td><td>string</td><td>YES</td><td>The id of Curator's Quoted Publication, such as 0x8d11-0x07-DA-1cdac4db</td></tr></tbody></table>

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

const result = await lensOpenCuration.register(26, '0x49-0x01-DA-779542b8')
```
{% endcode %}

## Example Returns

```json
register lens curation succeed
```
