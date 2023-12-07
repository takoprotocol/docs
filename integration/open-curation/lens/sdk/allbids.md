# allBids

<table><thead><tr><th width="160">SDK</th><th>allBids</th></tr></thead><tbody><tr><td>Description</td><td>Retrieve the bids feed</td></tr><tr><td>Nature</td><td>Property of Class</td></tr></tbody></table>

## Example Code

{% code fullWidth="false" %}
```typescript
import { CONSTANT, TakoOpenCuration } from 'tako-open-curation'

const tako = new TakoOpenCuration(CONSTANT.Network.TESTNET)
const lensOpenCuration = tako.lensOpenCuration

const query = await lensOpenCuration.allBids.DESC.status(CONSTANT.OpenCurationAllBidsStatus.Pending)
const pendingBids = await query.get()

// sorted result
// const query = await lensOpenCuration.allBids.sort('create_at').ASC.status(CONSTANT.OpenCurationAllBidsStatus.All)

// Querying by a specified quantity
// const query = await lensOpenCuration.allBids.limit(3).DESC.status(CONSTANT.OpenCurationAllBidsStatus.All)
```
{% endcode %}

## Example Returns

```json
result {
  bids: [
    {
      id: 35,
      index: 2,
      content_id: '0x01bd-0x01-DA-da16dd1b',
      bid_token: '0x0000000000000000000000000000000000000000',
      bid_address: '0xC439530f6A0582Bc09da70A3e52Ace7dF4b58A32',
      bid_amount: '120',
      bid_time: 1700210601,
      curator_id: 445,
      curator_content_id: '0x01bd-0x01-DA-29898514',
      state: 'Pass',
      bid_type: 'QuotedPublication',
      block_number: 0,
      others: {},
      events: [Object],
      create_at: 1700210601,
      update_at: 1700469727
    },
    {
      id: 36,
      index: 3,
      content_id: '0x01bd-0x01-DA-84dddefe',
      bid_token: '0x0000000000000000000000000000000000000000',
      bid_address: '0xC439530f6A0582Bc09da70A3e52Ace7dF4b58A32',
      bid_amount: '10',
      bid_time: 1700632484,
      curator_id: 0,
      curator_content_id: '',
      state: 'Pending',
      bid_type: 'QuotedPublication',
      block_number: 0,
      others: {},
      events: [Object],
      create_at: 1700632484,
      update_at: 1700632484
    }
  ],
  total: 22
}

```
