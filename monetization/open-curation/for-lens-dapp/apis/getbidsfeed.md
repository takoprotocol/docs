# GetBidsFeed

## API

<table><thead><tr><th width="160">API</th><th>/v2/lens/open_curation/all_bids</th></tr></thead><tbody><tr><td>Title</td><td>GetBidsFeed</td></tr><tr><td>Description</td><td>Retrieve the bids feed</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="139">Name</th><th width="115">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileIds</td><td>int[]</td><td>YES</td><td>The lens profile id list of the curators for the bids</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, offsett 5 means that the first 5 rows of the query result will be skipped.</td></tr><tr><td>sort</td><td>string</td><td>NO</td><td>Can sort by "bid_amount", "create_at", "update_at", default to "bid_amount"</td></tr><tr><td>sortType</td><td>string</td><td>NO</td><td>“desc” or “asc”, default to “desc”. Arrange in ascending or descending order.</td></tr><tr><td>status</td><td>string</td><td>NO</td><td>The status of the bid. “Pending”, “Pass”, “Cancel”.<br>All data will be queried if the status is not included in the request parameters.</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/open_curation/all_bids' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "limit": 3,
    "offset": 0,
    "sort": "create_at",
    "sortType": "desc",
    "status": "Pending"
  }'
```

#### Request URL

`https://api.tako.so/v2/lens/open_curation/all_bids`

### Response

```
{
  "status": "success",
  "data": {
    "bids": [
      {
        "id": 903,
        "index": 13,
        "content_id": "0xae-0x08-DA-60c4916e",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xCe41cdCCA1849CaD58DaACc6005B1990Be04e1F0",
        "bid_amount": "161000000000000",
        "bid_time": 1700644794,
        "curator_id": 0,
        "curator_content_id": "",
        "state": "Pending",
        "bid_type": "QuotedPublication",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0x63a0232bbc65afc1db82f134d3a40f6b0f0e590aa57aed839766fdc36474c46c",
            "event_name": "addBidEvent",
            "block_number": 42702173,
            "block_timestamp": 1700644794
          }
        },
        "create_at": 1700644794,
        "update_at": 1700644794
      },
      {
        "id": 807,
        "index": 10,
        "content_id": "0x01bd-0x01-DA-84dddefe",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xC439530f6A0582Bc09da70A3e52Ace7dF4b58A32",
        "bid_amount": "42000000000000000",
        "bid_time": 1700644642,
        "curator_id": 0,
        "curator_content_id": "",
        "state": "Pending",
        "bid_type": "QuotedPublication",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0xfc3c067c63e77538641fe174001b0ae0b9b41362c00fdd65c9ef5e95fe34cfc8",
            "event_name": "addBidEvent",
            "block_number": 42702114,
            "block_timestamp": 1700644642
          }
        },
        "create_at": 1700644642,
        "update_at": 1700644642
      },
      {
        "id": 808,
        "index": 11,
        "content_id": "0x01bd-0x01-DA-84dddefe",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xC439530f6A0582Bc09da70A3e52Ace7dF4b58A32",
        "bid_amount": "13",
        "bid_time": 1700644642,
        "curator_id": 0,
        "curator_content_id": "",
        "state": "Pending",
        "bid_type": "QuotedPublication",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0xfc3c067c63e77538641fe174001b0ae0b9b41362c00fdd65c9ef5e95fe34cfc8",
            "event_name": "addBidEvent",
            "block_number": 42702114,
            "block_timestamp": 1700644642
          }
        },
        "create_at": 1700644642,
        "update_at": 1700644642
      }
    ],
    "total": 6
  }
}
```
