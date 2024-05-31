# GetProfileAndKey

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/portfolio/view</th></tr></thead><tbody><tr><td>Title</td><td>GetProfileAndKey</td></tr><tr><td>Description</td><td>Get user's profile infomation and the status of his profile key</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YES</td><td>"lens" or "farcaster"</td></tr><tr><td>addr</td><td>string</td><td>YES</td><td>The user's EVM wallet address</td></tr><tr><td>profile_id</td><td>string</td><td>YES</td><td>The Lens profile id or Farcaster FID of the user</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/token/profile/v1/portfolio/view' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "addr": "0xcb093137a3098dEbBCe9C5D416D9A257914d9754",
    "ecosystem": "farcaster",
    "profile_id": 10001
  }'
```

#### Request URL

`https://api.tako.so/token/profile/v1/portfolio/view`

### Response

```json
{
  "code": 0,
  "msg": "OK",
  "data": {
    "initiated": true,
    "share_price": "70833333333333",
    "holder_count": 2,
    "profile": {
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
    "comparison": {
      "now_supply": 3,
      "compared_to": "24h0m0s",
      "now_price": "20843333333333",
      "type": "flat",
      "yield": 0,
      "content_id": "10001",
      "token": "0x0000000000000000000000000000000000000000",
      "symbol": "ETH",
      "decimal": 18
    }
  },
  "ts": "2023-12-21 12:42:31.77099"
}
```
