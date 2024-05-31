# GetClaimable

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/{ecosystem}/claimable</th></tr></thead><tbody><tr><td>Title</td><td>GetClaimable</td></tr><tr><td>Description</td><td>Get the claimable fee</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YES</td><td>Only support "farcaster" now</td></tr><tr><td>addr</td><td>string</td><td>YES</td><td>The user's EVM wallet address</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/token/profile/v1/farcaster/claimable' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "addr": "0xa75648322b4a6B6d55159f3cBB8a204faA9f53CD"
  }'
```

#### Request URL

`https://api.tako.so/token/profile/v1/farcaster/claimable`

### Response

```json
{
  "code": 0,
  "ts": "2023-12-21 16:18:58.94316",
  "msg": "OK",
  "data": 120000
}
```
