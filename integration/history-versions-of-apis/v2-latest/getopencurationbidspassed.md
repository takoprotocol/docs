# getOpenCurationBidsPassed

## API

<table><thead><tr><th width="160">API</th><th>/v2/lens/open_curation/passed_bids</th></tr></thead><tbody><tr><td>Title</td><td>getOpenCurationBidsPassed</td></tr><tr><td>Description</td><td>The curation has already ended, and the curator has claimed the reward</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="113">Name</th><th width="82">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, offset 5 means that the first 5 rows of the query result will be skipped.</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/v2/lens/open_curation/passed_bids' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/v2/lens/open_curation/passed_bids`

### Response

```
{
  "status": "success",
  "data": {
    "bids": [
      {
        "id": 269,
        "index": 1,
        "content_id": "0x8d10-0x06-DA-a915e490",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xCe41cdCCA1849CaD58DaACc6005B1990Be04e1F0",
        "bid_amount": "161000000000000",
        "bid_time": 1697450747,
        "curator_id": 36113,
        "curator_content_id": "0x8d11-0x07-DA-9f71b8a3",
        "state": "Pass",
        "bid_type": "QuotedPublication",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0xcb487db8adbeef2ddb50f9fce6bf7d9c198637a02174e3bba78ab6ef1dcc5c8b",
            "event_name": "addBidEvent",
            "block_number": 41264296,
            "block_timestamp": 1697450747
          },
          "modifiBidEventPass": {
            "state": "Pass",
            "tx_hash": "0x80a2cd7177c0c5e9fc2274db5e090dba610651d52622fc015caacc1e3a3ebd27",
            "event_name": "modifiBidEvent",
            "block_number": 41291074,
            "block_timestamp": 1697512555
          }
        },
        "create_at": 1697450747,
        "update_at": 1697512555
      }
    ],
    "total": 1
  }
}
```
