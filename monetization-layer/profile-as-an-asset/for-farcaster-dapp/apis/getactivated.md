# GetActivated

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/shares/activated</th></tr></thead><tbody><tr><td>Title</td><td>GetActivatied</td></tr><tr><td>Description</td><td>Retrieve the key and profile information of the Farcaster profile that has already been activated</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>NO</td><td>"lens" or "farcaster"</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, offsett 5 means that the first 5 rows of the query result will be skipped.</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/token/profile/v1/shares/activated?limit=10&ecosystem=farcaster' \
  -H 'accept: application/json'
```

#### Request URL

`https://testapi.tako.so/token/profile/v1/shares/activated?limit=10&ecosystem=farcaster`

### Response

```json
{
  "code": 0,
  "msg": "OK",
  "data": {
    "trades": null,
    "items": [
      {
        "now_supply": 3,
        "compared_to": "24h0m0s",
        "now_price": "70845666666666",
        "type": "flat",
        "yield": 0,
        "content_id": "10001",
        "token": "0x0000000000000000000000000000000000000000",
        "symbol": "ETH",
        "decimal": 18,
        "create_at": 1703145101
      },
      {
        "now_supply": 3,
        "compared_to": "24h0m0s",
        "now_price": "10000000",
        "type": "flat",
        "yield": 0,
        "content_id": "10002",
        "token": "0x0000000000000000000000000000000000000000",
        "symbol": "ETH",
        "decimal": 18,
        "create_at": 1702978279
      },
      {
        "now_supply": 6,
        "compared_to": "24h0m0s",
        "now_price": "345678920",
        "type": "flat",
        "yield": 0,
        "content_id": "10003",
        "token": "0x0000000000000000000000000000000000000000",
        "symbol": "ETH",
        "decimal": 18,
        "create_at": 1702978267
      }
    ],
    "profiles": {
      "10001": {
        "fid": 10001,
        "username": "demo1",
        "displayName": "demo1",
        "pfp": {
          "url": "https://demo.com/demo1.jpg",
          "verified": false
        },
        "profile": {
          "bio": {
            "text": "",
            "mentions": []
          },
          "location": {
            "placeId": "",
            "description": ""
          }
        },
        "followerCount": 8,
        "followingCount": 51,
        "activeOnFcNetwork": false,
        "referrerUsername": "",
        "viewerContext": {
          "following": false,
          "followedBy": false,
          "canSendDirectCasts": true,
          "hasUploadedInboxKeys": true
        },
        "extras": {
          "fid": 10001,
          "custodyAddress": "0xcb093137a3098dEbBCe9C5D416D9A257914d9754"
        }
      },
      "10002": {
        "fid": 10002,
        "username": "demo2",
        "displayName": "demo2",
        "pfp": {
          "url": "https://demo.com/demo2.jpg",
          "verified": false
        },
        "profile": {
          "bio": {
            "text": "",
            "mentions": []
          },
          "location": {
            "placeId": "",
            "description": ""
          }
        },
        "followerCount": 19,
        "followingCount": 9,
        "activeOnFcNetwork": false,
        "referrerUsername": "",
        "viewerContext": {
          "following": false,
          "followedBy": false,
          "canSendDirectCasts": true,
          "hasUploadedInboxKeys": true
        },
        "extras": {
          "fid": 10002,
          "custodyAddress": "0x1E76aF80cc21e1E3cf8F7d3C170D585D265E0a89"
        }
      },
      "10003": {
        "fid": 10003,
        "username": "demo3",
        "displayName": "demo3",
        "pfp": {
          "url": "https://demo.com/demo3.jpg",
          "verified": false
        },
        "profile": {
          "bio": {
            "text": "",
            "mentions": []
          },
          "location": {
            "placeId": "",
            "description": ""
          }
        },
        "followerCount": 14,
        "followingCount": 39,
        "activeOnFcNetwork": false,
        "referrerUsername": "",
        "viewerContext": {
          "following": false,
          "followedBy": false,
          "canSendDirectCasts": false,
          "hasUploadedInboxKeys": true
        },
        "extras": {
          "fid": 10003,
          "custodyAddress": "0xE9162B421D272714613E7a528e7ED5Cd11fbC196"
        }
      }
    },
    "total": 3
  },
  "ts": "2023-12-21 12:50:08.54647"
}
```
