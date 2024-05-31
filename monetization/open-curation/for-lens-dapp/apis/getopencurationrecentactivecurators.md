# getOpenCurationRecentActiveCurators

## API

<table><thead><tr><th width="170">API</th><th>/v2/lens/open_curation/recent/curators</th></tr></thead><tbody><tr><td>Title</td><td>getOpenCurationRecentActiveCurators</td></tr><tr><td>Description</td><td>Retrieve the recent curators that have accepted bids</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/v2/lens/open_curation/recent/curators' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/v2/lens/open_curation/recent/curators`

### Response

```
{
  "status": "success",
  "data": [
    {
      "item": {
        "content_id": "",
        "bid_time": 0,
        "curator_id": 36113,
        "curator_content_id": "",
        "id": 269,
        "index": 0,
        "bid_token": "",
        "bid_address": "",
        "bid_amount": "161000000000000",
        "bid_type": "",
        "others": null,
        "events": null,
        "create_at": 0,
        "update_at": 1697512555
      },
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
      "curator_info": {
        "last_bid_price": "161000000000000"
      }
    }
  ]
}
```
