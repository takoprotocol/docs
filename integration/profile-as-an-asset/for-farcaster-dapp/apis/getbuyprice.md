# GetBuyPrice

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/calculate/buy_price</th></tr></thead><tbody><tr><td>Title</td><td>GetBuyPrice</td></tr><tr><td>Description</td><td>Get buy price of the Key based on amount</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>creatorId</td><td>int</td><td>YES</td><td>The Farcaster FID of the creator</td></tr><tr><td>amount</td><td>int</td><td>YES</td><td>The amount of Key to be purchased</td></tr><tr><td>ecosystem</td><td>string</td><td>YES</td><td>Only suppports "farcaster"</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/token/profile/v1/calculate/buy_price?creatorId=10001&amount=1&ecosystem=farcaster' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/token/profile/v1/calculate/buy_price?creatorId=10001&amount=1&ecosystem=farcaster`

### Response

```json
{
  "code": 0,
  "ts": "2023-12-22 04:05:33.80184",
  "msg": "OK",
  "data": 127083333333334
}
```
