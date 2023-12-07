# GetRecentActiveCurators

## API

<table><thead><tr><th width="170">API</th><th>/v1/recent/curators</th></tr></thead><tbody><tr><td>Title</td><td>GetRecentActiveCurators</td></tr><tr><td>Description</td><td>Retrieve the recent Lens accounts that have received and accepted bids.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="110">Name</th><th width="97">Type</th><th width="114">Required</th><th>Description</th></tr></thead><tbody><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, OFFSET 5 means that the first 5 rows of the query result will be skipped.</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.takoyaki.so/v1/recent/curators?limit=5&offset=0' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.takoyaki.so/v1/recent/curators?limit=5&offset=0`

### Response

```json
{
  "status": "success",
  "data": [
    {
      "item": {
        "id": 17657,
        "index": 0,
        "ignores": null,
        "platform_type": "",
        "content_uri": "",
        "bid_token": "",
        "bid_address": "",
        "bid_amount": 0,
        "bid_expires": 0,
        "to_profiles": null,
        "curator_profile_id": 34971,
        "curator_pub_id": "",
        "bid_type": "",
        "others": null,
        "events": null,
        "create_at": 0,
        "update_at": 1690964462
      },
      "profile": {
        "id": "0x889b",
        "name": "",
        "bio": "",
        "attributes": [],
        "followNftAddress": "0xC4c4669b4ef2570A3E229e38C19f51b03B9e5C1d",
        "metadata": "",
        "isDefault": false,
        "picture": null,
        "handle": "enzo_si.test",
        "coverPicture": null,
        "ownedBy": "0x2a9D314900f6B8F19Ba7206BDA01bC495c2A08c9",
        "dispatcher": {
          "address": "0x6C1e1bC39b13f9E0Af9424D76De899203F47755F"
        },
        "stats": {
          "totalFollowers": 0,
          "totalFollowing": 1,
          "totalPosts": 10,
          "totalComments": 0,
          "totalMirrors": 4,
          "totalPublications": 14,
          "totalCollects": 2
        },
        "followModule": {
          "amount": {
            "asset": {
              "address": "0x9c3C9283D3e44854697Cd22D3Faa240Cfb032889",
              "decimals": 18,
              "name": "Wrapped Matic",
              "symbol": "WMATIC"
            },
            "value": "0.1"
          },
          "recipient": "0x2a9D314900f6B8F19Ba7206BDA01bC495c2A08c9",
          "type": "FeeFollowModule"
        }
      },
      "curator_info": {}
    },
    {
      "item": {
        "id": 17398,
        "index": 0,
        "ignores": null,
        "platform_type": "",
        "content_uri": "",
        "bid_token": "",
        "bid_address": "",
        "bid_amount": 10000000000000000,
        "bid_expires": 0,
        "to_profiles": null,
        "curator_profile_id": 35349,
        "curator_pub_id": "",
        "bid_type": "",
        "others": null,
        "events": null,
        "create_at": 0,
        "update_at": 1690963778
      },
      "profile": {
        "id": "0x8a15",
        "name": "",
        "bio": "",
        "attributes": [],
        "followNftAddress": null,
        "metadata": "",
        "isDefault": false,
        "picture": null,
        "handle": "lens0x7117.test",
        "coverPicture": null,
        "ownedBy": "0x7117c2e4681195F017E6710f07d56E588b8BBad1",
        "dispatcher": {
          "address": ""
        },
        "stats": {
          "totalFollowers": 0,
          "totalFollowing": 0,
          "totalPosts": 1,
          "totalComments": 0,
          "totalMirrors": 0,
          "totalPublications": 1,
          "totalCollects": 0
        },
        "followModule": null
      },
      "curator_info": {
        "last_bid_price": 10000000000000000
      }
    },
    {
      "item": {
        "id": 13120,
        "index": 0,
        "ignores": null,
        "platform_type": "",
        "content_uri": "",
        "bid_token": "",
        "bid_address": "",
        "bid_amount": 1000000000000000,
        "bid_expires": 0,
        "to_profiles": null,
        "curator_profile_id": 34370,
        "curator_pub_id": "",
        "bid_type": "",
        "others": null,
        "events": null,
        "create_at": 0,
        "update_at": 1690352753
      },
      "profile": {
        "id": "0x8642",
        "name": "",
        "bio": "",
        "attributes": [],
        "followNftAddress": null,
        "metadata": "",
        "isDefault": false,
        "picture": null,
        "handle": "lenstest1111.test",
        "coverPicture": null,
        "ownedBy": "0x793eC059cCc2Ceeb8c6748111550b23c4e0072Bb",
        "dispatcher": {
          "address": "0x6C1e1bC39b13f9E0Af9424D76De899203F47755F"
        },
        "stats": {
          "totalFollowers": 0,
          "totalFollowing": 0,
          "totalPosts": 23,
          "totalComments": 5,
          "totalMirrors": 24,
          "totalPublications": 52,
          "totalCollects": 0
        },
        "followModule": null
      },
      "curator_info": {
        "last_bid_price": 1000000000000000
      }
    }
  ]
}
```
