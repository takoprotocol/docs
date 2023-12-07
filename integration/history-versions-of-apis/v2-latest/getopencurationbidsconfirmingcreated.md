# getOpenCurationBidsConfirmingCreated

## API

<table><thead><tr><th width="162">API</th><th>/v2/lens/open_curation/get_bids_confirming_created</th></tr></thead><tbody><tr><td>Title</td><td>getOpenCurationBidsConfirmingCreated</td></tr><tr><td>Description</td><td>After bids are created and submitted, it needs to be confirmed by the Polygon network. To ensure data security, a certain number of blocks will be waited for before considering the bid data to be accurate and correct. This interface is used to query confirming bids created by bidders.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<mark style="color:red;">At least one of addresses and profileIds needs to be filled.</mark>

<table><thead><tr><th width="129">Name</th><th width="91">Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>addresses</td><td>string[]</td><td>NO</td><td>The EVM-compatible address list of the bidders</td></tr><tr><td>profileIds</td><td>int[]</td><td>NO</td><td>The lens profile id list of the bidders</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/open_curation/get_bids_confirming_created' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "profileIds": [
      36112
    ]
  }'
```

#### Request URL

`https://api.tako.so/v2/lens/open_curation/get_bids_confirming_created`

### Response

```
{
  "status": "success",
  "data": {
    "bids": [
      {
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
        "block_number": 41264329,
        "others": {},
        "events": {
          "addBidEvent": {
            "block_number": 41264329,
            "block_timestamp": 1697450817,
            "event_name": "addBidEvent",
            "state": "Pending",
            "tx_hash": "0xc710c476c18b7c1d4ec4e1b17d2f15c6eb18a47ea5597cfda0a9bb62d06cc7cf"
          }
        },
        "create_at": 1697450817,
        "update_at": 1697450817
      },
      {
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
        "block_number": 41264312,
        "others": {},
        "events": {
          "addBidEvent": {
            "block_number": 41264312,
            "block_timestamp": 1697450781,
            "event_name": "addBidEvent",
            "state": "Pending",
            "tx_hash": "0x0ece5d5c660725a625e23ae58808c9705ae1ed004f19e70ae3860993e41d5d55"
          }
        },
        "create_at": 1697450781,
        "update_at": 1697450781
      },
      {
        "index": 1,
        "content_id": "0x8d10-0x06-DA-a915e490",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xCe41cdCCA1849CaD58DaACc6005B1990Be04e1F0",
        "bid_amount": "161000000000000",
        "bid_time": 1697450747,
        "curator_id": 0,
        "curator_content_id": "",
        "state": "Pending",
        "bid_type": "QuotedPublication",
        "block_number": 41264296,
        "others": {},
        "events": {
          "addBidEvent": {
            "block_number": 41264296,
            "block_timestamp": 1697450747,
            "event_name": "addBidEvent",
            "state": "Pending",
            "tx_hash": "0xcb487db8adbeef2ddb50f9fce6bf7d9c198637a02174e3bba78ab6ef1dcc5c8b"
          }
        },
        "create_at": 1697450747,
        "update_at": 1697450747
      }
    ],
    "total": 3
  }
}
```
