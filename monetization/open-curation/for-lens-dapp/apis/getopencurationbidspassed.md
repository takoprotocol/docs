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
        "id": 1572,
        "index": 17,
        "content_id": "0xae-0x08-DA-bb2abe84",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0x0f9Ab2e48665487BE9e2f5EF238496Ef9213AE57",
        "bid_amount": "161000000000000",
        "bid_time": 1700649858,
        "curator_id": 180,
        "curator_content_id": "0xb4-0x08-DA-67cfa258",
        "state": "Pass",
        "bid_type": "QuotedPublication",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0x663bb6ebf56899ffc15c82d668fb72584b1b9764c4cc72d6914e6da4b2060132",
            "event_name": "addBidEvent",
            "block_number": 42704370,
            "block_timestamp": 1700649858
          },
          "modifiBidEventPass": {
            "state": "Pass",
            "tx_hash": "0xfeb28aab6bd5b0cafeb88a8d17c576afb9f8e68992fcc85a0dd5e4d524c6473d",
            "event_name": "modifiBidEvent",
            "block_number": 42731575,
            "block_timestamp": 1700710323
          }
        },
        "create_at": 1700649858,
        "update_at": 1700710323
      },
      {
        "id": 809,
        "index": 12,
        "content_id": "0x01bd-0x01-DA-84dddefe",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xC439530f6A0582Bc09da70A3e52Ace7dF4b58A32",
        "bid_amount": "52000000000000000",
        "bid_time": 1700644642,
        "curator_id": 1243,
        "curator_content_id": "0x04db-0x01-DA-cc5600fc",
        "state": "Pass",
        "bid_type": "QuotedPublication",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0xfc3c067c63e77538641fe174001b0ae0b9b41362c00fdd65c9ef5e95fe34cfc8",
            "event_name": "addBidEvent",
            "block_number": 42702114,
            "block_timestamp": 1700644642
          },
          "modifiBidEventPass": {
            "state": "Pass",
            "tx_hash": "0xf095b966f982f1b5291f697919a4dea90659a5baa7250bd8d508d205e6155a24",
            "event_name": "modifiBidEvent",
            "block_number": 42702514,
            "block_timestamp": 1700645562
          }
        },
        "create_at": 1700644642,
        "update_at": 1700645562
      },
      {
        "id": 807,
        "index": 10,
        "content_id": "0x01bd-0x01-DA-84dddefe",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xC439530f6A0582Bc09da70A3e52Ace7dF4b58A32",
        "bid_amount": "42000000000000000",
        "bid_time": 1700644642,
        "curator_id": 445,
        "curator_content_id": "0x01bd-0x01-DA-9323c7c9",
        "state": "Pass",
        "bid_type": "QuotedPublication",
        "block_number": 0,
        "others": {},
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0xfc3c067c63e77538641fe174001b0ae0b9b41362c00fdd65c9ef5e95fe34cfc8",
            "event_name": "addBidEvent",
            "block_number": 42702114,
            "block_timestamp": 1700644642
          },
          "modifiBidEventPass": {
            "state": "Pass",
            "tx_hash": "0xf095b966f982f1b5291f697919a4dea90659a5baa7250bd8d508d205e6155a24",
            "event_name": "modifiBidEvent",
            "block_number": 42702514,
            "block_timestamp": 1700645562
          }
        },
        "create_at": 1700644642,
        "update_at": 1700645562
      }
    ],
    "total": 10
  }
}
```
