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
    "addresses": [
      "0x0f9Ab2e48665487BE9e2f5EF238496Ef9213AE57"
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
        "index": 16,
        "content_id": "0xae-0x08-DA-4b5ae780",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0x0f9Ab2e48665487BE9e2f5EF238496Ef9213AE57",
        "bid_amount": "161000000000000",
        "bid_time": 1700648606,
        "curator_id": 0,
        "curator_content_id": "",
        "state": "Pending",
        "bid_type": "QuotedPublication",
        "block_number": 42703826,
        "others": {},
        "events": {
          "addBidEvent": {
            "block_number": 42703826,
            "block_timestamp": 1700648606,
            "event_name": "addBidEvent",
            "state": "Pending",
            "tx_hash": "0x38267ea061a651de0057fcea8ef0639e8d15346bab0a7b99c29e27536703dd70"
          }
        },
        "create_at": 1700648606,
        "update_at": 1700648606
      }
    ],
    "total": 1
  }
}
```
