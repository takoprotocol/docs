# GetHoldersByAddress

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/shares/holder/byaddr</th></tr></thead><tbody><tr><td>Title</td><td>GetHoldersByAddress</td></tr><tr><td>Description</td><td>Get the Key holders by address that owns a Farcaster or Lens profile</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YES</td><td>"lens" or "farcaster"</td></tr><tr><td>addr</td><td>string</td><td>YES</td><td>The user's EVM-wallet address</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, offsett 5 means that the first 5 rows of the query result will be skipped.</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/token/profile/v1/shares/holder/byaddr?addr=0x765754CCDa2bfC41e8Fd399Fdd4C076fd79c5545&limit=10&ecosystem=farcaster' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/token/profile/v1/shares/holder/byaddr?addr=`0x765754CCDa2bfC41e8Fd399Fdd4C076fd79c5545`&limit=10&ecosystem=farcaster`

### Response

```json
{
  "code": 0,
  "msg": "OK",
  "data": {
    "shares": [
      {
        "trader": "0xE9162B421D272714613E7a528e7ED5Cd11fbC196",
        "trader_id": "10001",
        "content_id": "10001",
        "net_amount": 2,
        "price": "70833333333333",
        "fake_price": "",
        "real_price": "",
        "latest_trade_at": 0
      },
      {
        "trader": "0x575C05eAaE30FC659719AC81346076d2fC6C05A3",
        "trader_id": "10002",
        "content_id": "10001",
        "net_amount": 1,
        "price": "70833333333333",
        "fake_price": "",
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
          "fid": 10001,
          "custodyAddress": "0xE9162B421D272714613E7a528e7ED5Cd11fbC196"
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
          "fid": 10002,
          "custodyAddress": "0x575C05eAaE30FC659719AC81346076d2fC6C05A3"
        }
      }
    },
    "link": {},
    "links": {},
    "members": {},
    "total": 2
  },
  "ts": "2023-12-21 13:00:46.59664"
}
```
