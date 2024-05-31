# GetHolders

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/content/{ecosystem}/{id}/holders</th></tr></thead><tbody><tr><td>Title</td><td>GetHolders</td></tr><tr><td>Description</td><td>Get the Key holders for a farcaster account</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YSE</td><td>"lens" or "farcaster" </td></tr><tr><td>id</td><td>string</td><td>YES</td><td>The Farcaster FID of the user</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/token/profile/v1/content/farcaster/10001/holders' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/token/profile/v1/content/farcaster/10001/holders`

### Response

```json
{
  "code": 0,
  "msg": "OK",
  "data": {
    "holders": [
      {
        "trader": "0x765754CCDa2bfC41e8Fd399Fdd4C076fd79c5545",
        "trader_id": "10001",
        "content_id": "10001",
        "net_amount": 2
      },
      {
        "trader": "0xd54703d1C82413B1eD23F47EcbBABEdC4879593F",
        "trader_id": "10002",
        "content_id": "10001",
        "net_amount": 1
      }
    ],
    "holder_count": 2,
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
    "profiles_map": null,
    "holds": 0,
    "sell_price": "0",
    "buy_price": "70833333333333",
    "token": "0x0000000000000000000000000000000000000000",
    "decimal": 18,
    "symbol": "ETH",
    "token_ids": null,
    "link": {},
    "links": {},
    "members": {}
  },
  "ts": "2023-12-21 13:20:20.85126"
}
```
