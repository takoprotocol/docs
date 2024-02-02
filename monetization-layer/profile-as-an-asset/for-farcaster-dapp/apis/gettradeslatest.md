# GetTradesLatest

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/trades/latest</th></tr></thead><tbody><tr><td>Title</td><td>GetTradesLatest</td></tr><tr><td>Description</td><td>Get the latest trades list</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YES</td><td>"lens" or "farcaster"</td></tr><tr><td>limit</td><td>int</td><td>YES</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, offsett 5 means that the first 5 rows of the query result will be skipped.</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/token/profile/v1/trades/latest?ecosystem=farcaster&limit=10' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/token/profile/v1/trades/latest?ecosystem=farcaster&limit=10`

### Response

```json
{
  "code": 0,
  "msg": "OK",
  "data": {
    "list": [
      {
        "id": 861,
        "is_buy": true,
        "trader": "0x080Fd1E11c86122077e86695ff36785dc07c5bBa",
        "trader_id": "211705",
        "type": 1,
        "price": "100000000000000",
        "content_id": "10001",
        "amount": 1,
        "supply": 1,
        "create_at": 1703225183
      },
      {
        "id": 860,
        "is_buy": true,
        "trader": "0x0340Df22E427961D378D0DA6Ef8a5C65779bBf9D",
        "trader_id": "",
        "type": 1,
        "price": "277098920",
        "content_id": "10002",
        "amount": 1,
        "supply": 7,
        "create_at": 1703218709
      },
      
    ],
    "profile": {
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
      }
    },
    "links": {},
    "members": {},
    "total": 29
  },
  "ts": "2023-12-22 07:37:48.97199"
}
```
