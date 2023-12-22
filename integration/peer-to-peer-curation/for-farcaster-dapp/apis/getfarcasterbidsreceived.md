# GetFarcasterBidsReceived

## API

<table><thead><tr><th width="157">API</th><th>/v2/farcaster/get_bids_received</th></tr></thead><tbody><tr><td>Title</td><td>GetFarcasterBidsReceived</td></tr><tr><td>Description</td><td>Retrieve the content created on Farcaster sent to you by others</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="162">Name</th><th width="98">Type</th><th width="111">Required</th><th>Description</th></tr></thead><tbody><tr><td>fids</td><td>int[]</td><td>YES</td><td>The Farcaster FID list of the curators</td></tr><tr><td>bidType</td><td>string[]</td><td>NO</td><td>"Casts", "Reply", "Recasts"<br>If the bidType is not included in the request parameters, all data will be queried.</td></tr><tr><td>includeIgnore</td><td>bool</td><td>NO</td><td>Should ignored content be included. Default to true</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, OFFSET 5 means that the first 5 rows of the query result will be skipped.</td></tr><tr><td>sort</td><td>string</td><td>NO</td><td>Can sort by "bid_amount", "create_at", "update_at", default to "bid_amount"</td></tr><tr><td>sortType</td><td>string</td><td>NO</td><td>“desc” or “asc”, default to “desc”. Arrange in ascending or descending order.</td></tr><tr><td>state</td><td>string</td><td>NO</td><td>The state of bid. “Pending”, “Pass”, “Cancel”.<br>If the state is not included in the request parameters, all data will be queried.</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/farcaster/get_bids_received' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "fids": [
      15706
    ],
    "bidType": [
      "Casts", "Recasts", "Reply"
    ],
    "includeIgnore": true,
    "limit": 5,
    "offset": 0,
    "sort": "create_at",
    "sortType": "desc",
    "state": "Cancel"
  }'
```

#### Request URL

`https://api.tako.so/v2/farcaster/get_bids_received`

### Response

```json
{
  "status": "success",
  "data": {
    "count": 2,
    "data": [
      {
        "parent_hash": "0xb9887c91aa180ad3f2ff293ae29554068edf0d96",
        "to_curators": [
          15706
        ],
        "curator_fid": 0,
        "curator_hash": "                                          ",
        "id": 1742,
        "index": 21,
        "content_uri": "ar://SNb1k9zCEtHeGW-lsFYkNI014P7Xxm8tcL-wveltfvg",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0x4971EDC57A412E8Da8f0bA016bA2309bd99264f5",
        "bid_amount": "0",
        "bid_expires": 1694790029,
        "state": "Pending",
        "bid_type": "Reply",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0xac7067dcb7f1515f10d6c47b63d30738d14740bd80bf1ab2ec5bb7daa7371787",
            "event_name": "addBidEvent",
            "block_number": 109574026,
            "block_timestamp": 1694746829
          }
        },
        "create_at": 1694746829,
        "update_at": 1694746829,
        "is_ignored": false
      },
      {
        "parent_hash": "0xde33643575401fb04caa9a60c5cccf0b37261880",
        "to_curators": [
          15706
        ],
        "curator_fid": 0,
        "curator_hash": "                                          ",
        "id": 560,
        "index": 9,
        "content_uri": "ar://iulWApzm7SUPUgmIG3TYcl0wOebr5N63_5nVfNKSmb4",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0x47Fcef6259d058BaB9389819E683A957ff89AD0a",
        "bid_amount": "0",
        "bid_expires": 1694638433,
        "state": "Pending",
        "bid_type": "Reply",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0x52c6ab568b3f8d32fce04f8e82f778ac237a3f9c38e8a1f9e19e790b9df42fd0",
            "event_name": "addBidEvent",
            "block_number": 109498228,
            "block_timestamp": 1694595233
          }
        },
        "create_at": 1694595233,
        "update_at": 1694595233,
        "is_ignored": false
      }
    ],
    "ecosystem": "farcaster"
  }
}
```
