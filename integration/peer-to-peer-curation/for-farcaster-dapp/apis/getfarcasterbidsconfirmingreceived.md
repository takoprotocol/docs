# GetFarcasterBidsConfirmingReceived

## API

<table><thead><tr><th width="162">API</th><th>/v2/farcaster/get_bids_confirming_received</th></tr></thead><tbody><tr><td>Title</td><td>GetFarcasterBidsConfirmingReceived</td></tr><tr><td>Description</td><td>After bidders create and submit a bid to the curator, it needs to be confirmed by the Polygon network. To ensure data security, a certain number of blocks will be waited for before considering the bid data to be accurate and correct. This interface is used to query confirming bids received by curators.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="129">Name</th><th width="91">Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>fids</td><td>int[]</td><td>NO</td><td>The Farcaster FID list of the bidders</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/farcaster/get_bids_confirming_received' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "fids": [
      15706
    ]
  }'
```

#### Request URL

`https://api.tako.so/v2/farcaster/get_bids_confirming_received`

### Response

```json
{
  "status": "success",
  "data": {
    "bids": [
      {
        "parent_hash": "0x611ef1cf238f91c9131ab426a45fac12cb17d026",
        "to_curators": [
          15706
        ],
        "curator_fid": 0,
        "curator_hash": "",
        "index": 24,
        "content_uri": "",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0x4971EDC57A412E8Da8f0bA016bA2309bd99264f5",
        "bid_amount": "100000000",
        "bid_expires": 1695412109,
        "state": "Pending",
        "bid_type": "Recast",
        "block_number": 109885066,
        "others": {},
        "events": {
          "addBidEvent": {
            "block_number": 109885066,
            "block_timestamp": 1695368909,
            "event_name": "addBidEvent",
            "state": "Pending",
            "tx_hash": "0xf52bb8b0874ccc872a65df59fb02780a19dc6c6ad324edc7a184953c849929b5"
          }
        },
        "create_at": 1695368909,
        "update_at": 1695368909,
        "is_ignored": false
      }
    ],
    "total": 1
  }
}
```
