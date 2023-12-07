# getOpenCurationBidsCreated

## API

<table><thead><tr><th width="162">API</th><th>/v2/lens/open_curation/get_bids_created</th></tr></thead><tbody><tr><td>Title</td><td>getOpenCurationBidsCreated</td></tr><tr><td>Description</td><td>Retrieve the bids created by the bidders on Lens</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="139">Name</th><th width="115">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileIds</td><td>int[]</td><td>YES</td><td>The lens profile id list of the bidders</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, offsett 5 means that the first 5 rows of the query result will be skipped.</td></tr><tr><td>sort</td><td>string</td><td>NO</td><td>Can sort by "bid_amount", "create_at", "update_at", default to "bid_amount"</td></tr><tr><td>sortType</td><td>string</td><td>NO</td><td>“desc” or “asc”, default to “desc”. Arrange in ascending or descending order.</td></tr><tr><td>state</td><td>string</td><td>NO</td><td>The state of bid. “Pending”, “Pass”, “Cancel”.<br>If the state is not included in the request parameters, all data will be queried.</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/open_curation/get_bids_created' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "limit": 5,
  "offset": 0,
  "profileIds": [
      36112
    ],
    "sort": "create_at",
    "sortType": "desc",
    "state": "Pending"
  }'
```

#### Request URL

`https://api.tako.so/v2/lens/open_curation/get_bids_created`

### Response

```
{
  "status": "success",
  "data": {
    "bids": [
      {
        "id": 34,
        "index": 2,
        "content_id": "0x8d10-0x06-DA-cc6b21ba",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xCe41cdCCA1849CaD58DaACc6005B1990Be04e1F0",
        "bid_amount": "120000000000000",
        "bid_time": 1697013419,
        "curator_id": 0,
        "curator_content_id": "",
        "state": "Pending",
        "bid_type": "QuotedPublication",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0xddded576352df4ae594a0138e6d380e1fc33704c20085be740422af7e7594187",
            "event_name": "addBidEvent",
            "block_number": 41080721,
            "block_timestamp": 1697013419
          }
        },
        "create_at": 1697013419,
        "update_at": 1697013419
      },
      {
        "id": 1,
        "index": 1,
        "content_id": "0x8d10-0x05",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xCe41cdCCA1849CaD58DaACc6005B1990Be04e1F0",
        "bid_amount": "100000000000",
        "bid_time": 1696671482,
        "curator_id": 0,
        "curator_content_id": "",
        "state": "Pending",
        "bid_type": "QuotedPublication",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0x98cc7e7a09696acec9db7a6b76c5d3180d5b03e8b7a657c48743b8a35e1e931a",
            "event_name": "addBidEvent",
            "block_number": 40933242,
            "block_timestamp": 1696671482
          }
        },
        "create_at": 1696671482,
        "update_at": 1696671482
      }
    ],
    "total": 2
  }
}
```
