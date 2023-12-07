# getOpenCurationBidsCreated

## API

<table><thead><tr><th width="162">API</th><th>/v2/lens/open_curation/get_bids_created</th></tr></thead><tbody><tr><td>Title</td><td>getOpenCurationBidsCreated</td></tr><tr><td>Description</td><td>Retrieve the bids created by the bidders on Lens</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="139">Name</th><th width="115">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileIds</td><td>int[]</td><td>YES</td><td>The lens profile id list of the bidders</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, offsett 5 means that the first 5 rows of the query result will be skipped.</td></tr><tr><td>sort</td><td>string</td><td>NO</td><td>Can sort by "bid_amount", "create_at", "update_at", default to "bid_amount"</td></tr><tr><td>sortType</td><td>string</td><td>NO</td><td>“desc” or “asc”, default to “desc”. Arrange in ascending or descending order.</td></tr><tr><td>status</td><td>string</td><td>NO</td><td>The state of bid. “Pending”, “Pass”, “Cancel”.<br>If the state is not included in the request parameters, all data will be queried.</td></tr></tbody></table>

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
    "limit": 3,
    "offset": 0,
    "profileIds": [
      174
    ],
    "sort": "create_at",
    "sortType": "desc",
    "status": "Pending"
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
        "id": 1266,
        "index": 15,
        "content_id": "0xae-0x08-DA-155f6c65",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0x0f9Ab2e48665487BE9e2f5EF238496Ef9213AE57",
        "bid_amount": "161000000000000",
        "bid_time": 1700647900,
        "curator_id": 0,
        "curator_content_id": "",
        "state": "Pending",
        "bid_type": "QuotedPublication",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0x10945cff4d8f61e5bdd95940d563d21db73815ab7e4405aeef6a43104163155b",
            "event_name": "addBidEvent",
            "block_number": 42703524,
            "block_timestamp": 1700647900
          }
        },
        "create_at": 1700647900,
        "update_at": 1700647900
      }
    ],
    "total": 1
  }
}
```
