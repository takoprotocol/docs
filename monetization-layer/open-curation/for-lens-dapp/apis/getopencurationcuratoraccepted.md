# getOpenCurationCuratorAccepted

## API

<table><thead><tr><th width="160">API</th><th>/v2/lens/open_curation/curator/accepted</th></tr></thead><tbody><tr><td>Title</td><td>getOpenCurationCuratorAccepted</td></tr><tr><td>Description</td><td>Retrieve the curator's previous curation, and these curations are all the best and can ultimately claim rewards</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="113">Name</th><th width="82">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileId</td><td>string</td><td>NO</td><td>The Lens profile id of curator</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>cursor</td><td>int</td><td>NO</td><td>The id of bid. After calling this API, you will get the parameter next_cursor from the return value. When calling this API again, pass next_cursor as the value for the parameter cursor, which filters out data before the cursor and only queries data after the cursor.</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/v2/lens/open_curation/curator/accepted?profileId=36113&cursor=0' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/v2/lens/open_curation/curator/accepted?profileId=36113&cursor=0`

### Response

```
{
  "status": "success",
  "data": {
    "list": [
      {
        "id": 269,
        "index": 0,
        "content_id": "0x8d10-0x06-DA-a915e490",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xCe41cdCCA1849CaD58DaACc6005B1990Be04e1F0",
        "bid_amount": "161000000000000",
        "bid_time": 1697450747,
        "curator_id": 36113,
        "curator_content_id": "0x8d11-0x07-DA-9f71b8a3",
        "state": "",
        "bid_type": "QuotedPublication",
        "profile": {
          "id": "0x8d11",
          "name": "",
          "bio": "",
          "attributes": [],
          "followNftAddress": null,
          "metadata": "",
          "isDefault": false,
          "picture": null,
          "handle": "curator1.test",
          "coverPicture": null,
          "ownedBy": "0x87A4798567135aD8fF1d380df18DBb63dD2771c8",
          "dispatcher": {
            "address": "0x6C1e1bC39b13f9E0Af9424D76De899203F47755F"
          },
          "stats": {
            "totalFollowers": 0,
            "totalFollowing": 0,
            "totalPosts": 5,
            "totalComments": 0,
            "totalMirrors": 6,
            "totalPublications": 11,
            "totalCollects": 0
          },
          "followModule": null
        },
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
      }
    ],
    "has_more": false,
    "next_cursor": 0
  }
}
```
