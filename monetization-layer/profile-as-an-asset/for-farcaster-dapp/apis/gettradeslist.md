# GetTradesList

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/trades/list</th></tr></thead><tbody><tr><td>Title</td><td>GetTradesList</td></tr><tr><td>Description</td><td>Get trades list based on custom conditions</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="194">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YES</td><td>"lens" or "farcaster"</td></tr><tr><td>limit</td><td>int</td><td>YES</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, offsett 5 means that the first 5 rows of the query result will be skipped.</td></tr><tr><td>addr</td><td>string</td><td>YES</td><td>The user's EVM wallet address</td></tr><tr><td>with_your_keys</td><td>bool</td><td>NO</td><td>Trades list for the activated keys at addr</td></tr><tr><td>with_your_holdings</td><td>bool</td><td>NO</td><td>Trades list for the keys held by addr</td></tr><tr><td>with_your_trades</td><td>bool</td><td>NO</td><td>Trades list for the trades made by addr</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://testapi.tako.so/token/profile/v1/trades/list?ecosystem=farcaster&limit=10&addr=0x0340Df22E427961D378D0DA6Ef8a5C65779bBf9D&with_your_keys=false&with_your_holdings=false&with_your_trades=true' \
  -H 'accept: application/json'
```

#### Request URL

\
`https://testapi.tako.so/token/profile/v1/trades/list?ecosystem=farcaster&limit=10&addr=`0x0340Df22E427961D378D0DA6Ef8a5C65779bBf9D`&with_your_keys=false&with_your_holdings=false&with_your_trades=true`

### Response

```json
{
  "code": 0,
  "msg": "OK",
  "data": {
    "list": [
      {
        "id": 833,
        "is_buy": true,
        "trader": "0x940314ca8BA65d956617E9f7043E4641d0FB0a94",
        "trader_id": "",
        "type": 1,
        "price": "127090482",
        "content_id": "10001",
        "amount": 1,
        "supply": 5,
        "create_at": 1703007289
      },
      {
        "id": 832,
        "is_buy": true,
        "trader": "0x5284F831Da9e5A13eCE18821025F90725780e64B",
        "trader_id": "16889",
        "type": 1,
        "price": "20000000",
        "content_id": "10002",
        "amount": 2,
        "supply": 2,
        "create_at": 1702907019
      }
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
    "members": {
      "0x940314ca8BA65d956617E9f7043E4641d0FB0a94": {
        "nickname": "demox",
        "avatar": ""
      },
      "0x5284F831Da9e5A13eCE18821025F90725780e64B": {
        "nickname": "demoy",
        "avatar": ""
      }
    },
    "total": 3
  },
  "ts": "2023-12-19 17:46:07.32364"
}
```
