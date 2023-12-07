# GetBidsFeed

## API

<table><thead><tr><th width="160">API</th><th>/v2/lens/open_curation/all_bids</th></tr></thead><tbody><tr><td>Title</td><td>GetBidsFeed</td></tr><tr><td>Description</td><td>Retrieve the bids feed</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="139">Name</th><th width="115">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileIds</td><td>int[]</td><td>YES</td><td>The lens profile id list of the bidders</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, offsett 5 means that the first 5 rows of the query result will be skipped.</td></tr><tr><td>sort</td><td>string</td><td>NO</td><td>Can sort by "bid_amount", "create_at", "update_at", default to "bid_amount"</td></tr><tr><td>sortType</td><td>string</td><td>NO</td><td>“desc” or “asc”, default to “desc”. Arrange in ascending or descending order.</td></tr><tr><td>state</td><td>string</td><td>NO</td><td>The state of the bid. “Pending”, “Pass”, “Cancel”.<br>All data will be queried if the state is not included in the request parameters.</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/open_curation/all_bids' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "limit": 0,
    "offset": 0,
    "profileIds": [
      36112
    ],
    "sort": "desc",
    "sortType": "bid_amount"
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
        "id": 281,
        "index": 2,
        "content_id": "0x8d10-0x06-DA-25909736",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xCe41cdCCA1849CaD58DaACc6005B1990Be04e1F0",
        "bid_amount": "161000000000000",
        "bid_time": 1697450781,
        "curator_id": 0,
        "curator_content_id": "",
        "state": "Pending",
        "bid_type": "QuotedPublication",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0x0ece5d5c660725a625e23ae58808c9705ae1ed004f19e70ae3860993e41d5d55",
            "event_name": "addBidEvent",
            "block_number": 41264312,
            "block_timestamp": 1697450781
          }
        },
        "create_at": 1697450781,
        "update_at": 1697450781
      },
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
      },
      {
        "id": 300,
        "index": 3,
        "content_id": "0x8d10-0x06-DA-367868ca",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xCe41cdCCA1849CaD58DaACc6005B1990Be04e1F0",
        "bid_amount": "161000000000000",
        "bid_time": 1697450817,
        "curator_id": 0,
        "curator_content_id": "",
        "state": "Pending",
        "bid_type": "QuotedPublication",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0xc710c476c18b7c1d4ec4e1b17d2f15c6eb18a47ea5597cfda0a9bb62d06cc7cf",
            "event_name": "addBidEvent",
            "block_number": 41264329,
            "block_timestamp": 1697450817
          }
        },
        "create_at": 1697450817,
        "update_at": 1697450817
      }
    ],
    "total": 3
  }
}
```
