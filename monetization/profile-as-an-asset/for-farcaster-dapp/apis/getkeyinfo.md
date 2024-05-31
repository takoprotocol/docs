# GetKeyInfo

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/shares/info</th></tr></thead><tbody><tr><td>Title</td><td>GetKeyInfo</td></tr><tr><td>Description</td><td>Get the details of the user's Key</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YES</td><td>"lens" or "farcaster"</td></tr><tr><td>creatorId</td><td>int</td><td>YES</td><td>The FID of farcaster or Lens Profile ID</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/token/profile/v1/shares/info?ecosystem=farcaster&creatorId=10001' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/token/profile/v1/shares/info?ecosystem=farcaster&creatorId=10001`

### Response

```json
{
  "code": 0,
  "ts": "2023-12-21 13:25:04.93853",
  "msg": "OK",
  "data": {
    "item": {
      "now_supply": 3,
      "compared_to": "24h0m0s",
      "now_price": "2250000000000000000",
      "type": "rise",
      "yield": 8,
      "content_id": "10001",
      "token": "0x0000000000000000000000000000000000000000",
      "symbol": "MATIC",
      "decimal": 18,
      "create_at": 1703145198
    },
    "profile": {
      "activeOnFcNetwork": false,
      "displayName": "demo1",
      "fid": 10001,
      "followerCount": 19,
      "followingCount": 9,
      "pfp": {
        "url": "https://demo.com/demo1.jpg",
        "verified": false
      },
      "profile": {
        "bio": {
          "mentions": [],
          "text": ""
        },
        "location": {
          "description": "",
          "placeId": ""
        }
      },
      "username": "10001",
      "viewerContext": {
        "canSendDirectCasts": false,
        "followedBy": false,
        "following": false,
        "hasUploadedInboxKeys": true
      }
    }
  }
}
```
