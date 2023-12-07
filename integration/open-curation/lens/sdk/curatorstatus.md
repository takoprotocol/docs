# curatorStatus()

<table><thead><tr><th width="160">SDK</th><th>curatorStatus()</th></tr></thead><tbody><tr><td>Description</td><td>Check the curation status of a bid</td></tr><tr><td>Nature</td><td>Method of Class</td></tr></tbody></table>

## Parameters

<table><thead><tr><th width="136.33333333333331">Name</th><th width="169">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>number</td><td>The index of bid</td></tr><tr><td>profileId</td><td>number</td><td>The curator’s Lens profile id</td></tr></tbody></table>

## Example Code

{% code fullWidth="false" %}
```typescript
import { CONSTANT, TakoOpenCuration } from 'tako-open-curation'

const tako = new TakoOpenCuration(CONSTANT.Network.TESTNET)
const lensOpenCuration = tako.lensOpenCuration

const result = await lensOpenCuration.curatorStatus(26, 72)
```
{% endcode %}

## Example Returns

```json
{ 
  description: 'in-progress',
  index: 27,
  profileId: 189,
  status: 3
}
```

```json
{
  description: 'no register info found',
  index: 1,
  profileId: 71,
  status: 0
}
```

```json
{
  description: 'unregistered',
  index: 27,
  profileId: 186,
  status: 4
}
```
