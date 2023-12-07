# GetLensCuratorAccepted

## API

<table><thead><tr><th width="160">API</th><th>/v2/lens/curator/accepted</th></tr></thead><tbody><tr><td>Title</td><td>GetLensCuratorAccepted</td></tr><tr><td>Description</td><td>Retrieve the last 10 completed bids</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="113">Name</th><th width="82">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileId</td><td>string</td><td>NO</td><td>The Lens profile id of curator</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>cursor</td><td>int</td><td>NO</td><td>The id of bid. After calling this API, you will get the parameter next_cursor from the return value. When calling this API again, pass next_cursor as the value for the parameter cursor, which filters out data before the cursor and only queries data after the cursor.</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/v2/lens/curator/accepted?profileId=36113&cursor=0'
```

#### Request URL

`https://api.tako.so/v2/lens/curator/accepted`

### Response

```json
{
  "status": "success",
  "data": {
    "list": [
      {
        "id": 19587,
        "index": 0,
        "platform_type": "momoka",
        "content_uri": "",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xCe41cdCCA1849CaD58DaACc6005B1990Be04e1F0",
        "bid_amount": 1000000000000,
        "curator_profile_id": 36113,
        "curator_pub_id": "0x8d11-0x01-DA-2e031960",
        "state": "",
        "bid_type": "Mirror",
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
            "totalPosts": 0,
            "totalComments": 0,
            "totalMirrors": 1,
            "totalPublications": 1,
            "totalCollects": 0
          },
          "followModule": null
        },
        "events": {
          "addBidMomokaEvent": {
            "state": "Pending",
            "tx_hash": "0xdc6a0bb00bac372f491f20221ac02ab15749045c0eae6a9a616ee9645105f9fc",
            "event_name": "addBidMomokaEvent",
            "block_number": 38579027,
            "block_timestamp": 1691030436
          },
          "modifiBidMomokaEventPass": {
            "state": "Pass",
            "tx_hash": "0x84036c1343faa17ab3d87cf0db72b7057355fededb54b1fc6136a31515592883",
            "event_name": "modifiBidMomokaEvent",
            "block_number": 38585588,
            "block_timestamp": 1691045429
          }
        },
        "create_at": 1691030436,
        "update_at": 1691045429
      }
    ],
    "has_more": false,
    "next_cursor": 0
  }
}
```
