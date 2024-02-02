# GetAssets

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/portfolio/me</th></tr></thead><tbody><tr><td>Title</td><td>GetAssets</td></tr><tr><td>Description</td><td>Get user's assets</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YES</td><td>"lens" or "farcaster"</td></tr><tr><td>addr</td><td>string</td><td>YES</td><td>The user's EVM wallet address with the social profile</td></tr><tr><td>profile_id</td><td>string</td><td>YES</td><td>The Lens profile id or Farcaster FID of the user</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/token/profile/v1/portfolio/me' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "addr": "0xcb093137a3098dEbBCe9C5D416D9A257914d9754",
    "ecosystem": "farcaster",
    "profile_id": 10001
  }'
```

#### Request URL

`https://api.tako.so/token/profile/v1/portfolio/me`

### Response

```json
{
  "code": 0,
  "msg": "OK",
  "data": {
    "balance": "3349744377436924",
    "portfolio_value": "0",
    "fees_earned": "",
    "selloff": "0"
  },
  "ts": "2023-12-21 09:38:48.09303"
}
```
