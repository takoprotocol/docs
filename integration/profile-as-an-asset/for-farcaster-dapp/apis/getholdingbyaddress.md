# GetHoldingByAddress

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/shares/holding</th></tr></thead><tbody><tr><td>Title</td><td>GetHolding</td></tr><tr><td>Description</td><td>Get the holding keys of the address that activated</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YES</td><td>"lens" or "farcaster"</td></tr><tr><td>addr</td><td>string</td><td>YES</td><td>The user's EVM-wallet address</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, offsett 5 means that the first 5 rows of the query result will be skipped.</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/token/profile/v1/shares/holding?addr=0x765754CCDa2bfC41e8Fd399Fdd4C076fd79c5545&limit=10&ecosystem=farcaster' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/token/profile/v1/shares/holding?addr=`0x765754CCDa2bfC41e8Fd399Fdd4C076fd79c5545`&limit=10&ecosystem=farcaster`

### Response

```json
{
  "code": 0,
  "msg": "OK",
  "data": {
    "shares": [
      {
        "trader": "",
        "trader_id": "",
        "content_id": "10001",
        "net_amount": 1,
        "price": "195844349",
        "fake_price": "195844349",
        "real_price": "",
        "latest_trade_at": 0
      },
      {
        "trader": "",
        "trader_id": "",
        "content_id": "10002",
        "net_amount": 1,
        "price": "10000000",
        "fake_price": "10000000",
        "real_price": "",
        "latest_trade_at": 0
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
    },
    "members": null,
    "total": 2
  },
  "ts": "2023-12-21 13:13:33.27903"
}
```
