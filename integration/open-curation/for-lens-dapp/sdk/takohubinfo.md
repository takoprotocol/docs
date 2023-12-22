# takoHubInfo()

<table><thead><tr><th width="160">SDK</th><th>takoHubInfo()</th></tr></thead><tbody><tr><td>Description</td><td>Get contract of Tako Protocol</td></tr><tr><td>Nature</td><td>Method of Class</td></tr></tbody></table>

## Example Code

{% code fullWidth="false" %}
```typescript
import { CONSTANT, TakoOpenCuration } from 'tako-open-curation'

const tako = new TakoOpenCuration(CONSTANT.Network.TESTNET)
const lensOpenCuration = tako.lensOpenCuration

const hub = await lensOpenCuration.takoHubInfo()
```
{% endcode %}

## Example Returns

```json
{
  chain: 'mumbai',
  chain_id: 80001,
  contract: '0xC158A4319BC125e315120DbDfBEa8b8343aa3234'
}
```
