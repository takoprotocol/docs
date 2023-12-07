# GetLensCuratorLastBidPrice

## API

<table><thead><tr><th width="163">API</th><th>/v2/lens/curator/last_bid_price</th></tr></thead><tbody><tr><td>Title</td><td>GetLensCuratorLastBidPrice</td></tr><tr><td>Description</td><td>Retrieve the token amount from the last executed bid by the curator.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="168">Name</th><th width="80">Type</th><th width="112">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileIds</td><td>int[]</td><td>YES</td><td>The curator’s Lens profile id list</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/curator/last_bid_price' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "profileIds": [
      36113
    ]
  }'
```

#### Request URL

`https://api.tako.so/v2/lens/curator/last_bid_price`

### Response

```json
{
  "status": "success",
  "data": {
    "data": {
      "36113": {
        "last_bid_price": 1000000000000
      }
    }
  }
}
```
