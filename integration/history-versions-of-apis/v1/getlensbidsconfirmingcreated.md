# GetLensBidsConfirmingCreated

## API

<table><thead><tr><th width="162">API</th><th>/v1/get_lens_bids_confirming_created</th></tr></thead><tbody><tr><td>Title</td><td>GetLensBidsConfirmingCreated</td></tr><tr><td>Description</td><td>After bidders creating and submitting a bid to curator, it needs to be confirmed by the Polygon network. In order to ensure data security, a certain number of blocks will be waited for before considering the bid data to be accurate and correct. This interface is used to query confirming bids created by bidders.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

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
  'https://api.takoyaki.so/v1/get_lens_bids_confirming_created' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "profileIds": [
    36112
  ]
}'
```

#### Request URL

`https://api.takoyaki.so/v1/get_lens_bids_confirming_created`

### Response

```json
{
  "status": "success",
  "data": {
    "bids": [
      {
        "index": 70,
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
        "block_number": 38553832,
        "others": {
          "profileIdPointed": 36112,
          "pubIdPointed": 2
        },
        "events": {
          "addBidEvent": {
            "block_number": 38553832,
            "block_timestamp": 1690969382,
            "event_name": "addBidEvent",
            "state": "Pending",
            "tx_hash": "0xfef79bb3082eed54df52319cac60563bd7430d4c165f9927bcd362d33862e9f7"
          }
        },
        "create_at": 1690969382,
        "update_at": 1690969382,
        "is_ignored": false
      }
    ],
    "total": 1
  }
}
```
