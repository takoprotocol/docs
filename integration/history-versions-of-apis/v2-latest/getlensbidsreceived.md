# GetLensBidsReceived

## API

<table><thead><tr><th width="157">API</th><th>/v2/lens/get_bids_received</th></tr></thead><tbody><tr><td>Title</td><td>GetLensBidsReceived</td></tr><tr><td>Description</td><td>Retrieve the content created on Lens sent to you by others.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="162">Name</th><th width="98">Type</th><th width="111">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileIds</td><td>int[]</td><td>YES</td><td>The lens profile id list of the curators</td></tr><tr><td>bidType</td><td>string[]</td><td>NO</td><td>"Post", "Mirror", "Comment", "QuotedPublication"<br>If the bidType is not included in the request parameters, all data will be queried.</td></tr><tr><td>includeIgnore</td><td>bool</td><td>NO</td><td>Should ignored content be included. Default to true</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, OFFSET 5 means that the first 5 rows of the query result will be skipped.</td></tr><tr><td>sort</td><td>string</td><td>NO</td><td>Can sort by "bid_amount", "create_at", "update_at", default to "bid_amount"</td></tr><tr><td>sortType</td><td>string</td><td>NO</td><td>“desc” or “asc”, default to “desc”. Arrange in ascending or descending order.</td></tr><tr><td>state</td><td>string</td><td>NO</td><td>The state of bid. “Pending”, “Pass”, “Cancel”.<br>If the state is not included in the request parameters, all data will be queried.</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/get_bids_received' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "bidType": [
      "Post", "Mirror"
    ],
    "includeIgnore": true,
    "limit": 5,
    "offset": 0,
    "profileIds": [
      36113
    ],
    "sort": "id",
    "sortType": "desc",
    "state": "Pending"
  }'
```

#### Request URL

`https://api.tako.so/v2/lens/get_bids_received`

### Response

```json
{
  "status": "success",
  "data": {
    "count": 1,
    "data": [
      {
        "id": 18729,
        "index": 70,
        "ignores": [
          false
        ],
        "platform_type": "polygon",
        "content_uri": "",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xCe41cdCCA1849CaD58DaACc6005B1990Be04e1F0",
        "bid_amount": 1000000000000,
        "bid_expires": 1691012582,
        "to_profiles": [
          36113
        ],
        "curator_profile_id": 0,
        "curator_pub_id": "0x00",
        "state": "Pending",
        "bid_type": "Mirror",
        "others": {
          "pubIdPointed": 2,
          "profileIdPointed": 36112
        },
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0xfef79bb3082eed54df52319cac60563bd7430d4c165f9927bcd362d33862e9f7",
            "event_name": "addBidEvent",
            "block_number": 38553832,
            "block_timestamp": 1690969382
          }
        },
        "create_at": 1690969382,
        "update_at": 1690969382
      }
    ],
    "ecosystem": "lens"
  }
}
```
