# GetFarcasterCuratorLastBidPrice

## API

<table><thead><tr><th width="163">API</th><th>/v2/farcaster/curator/last_bid_price</th></tr></thead><tbody><tr><td>Title</td><td>GetFarcasterCuratorLastBidPrice</td></tr><tr><td>Description</td><td>Retrieve the token amount from the last executed bid by the curator</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="168">Name</th><th width="80">Type</th><th width="112">Required</th><th>Description</th></tr></thead><tbody><tr><td>fids</td><td>int[]</td><td>YES</td><td>The curator’s Farcaster FID list</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/farcaster/curator/last_bid_price' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "fids": [
      15706
    ]
  }'
```

#### Request URL

`https://api.tako.so/v2/farcaster/curator/last_bid_price`

### Response

```json
{
  "status": "success",
  "data": {
    "data": {
      "15706": {
        "last_bid_price": "0"
      }
    }
  }
}
```
