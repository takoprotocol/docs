# getOpenCurationCuratorLastBidPrice

## API

<table><thead><tr><th width="163">API</th><th>/v2/lens/open_curation/curator/last_bid_price</th></tr></thead><tbody><tr><td>Title</td><td>getOpenCurationCuratorLastBidPrice</td></tr><tr><td>Description</td><td>Retrieve the token amount from the last executed bid by the curator.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="168">Name</th><th width="80">Type</th><th width="112">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileIds</td><td>int[]</td><td>YES</td><td>The curator’s Lens profile id list</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/open_curation/curator/last_bid_price' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "profileIds": [
      180
    ]
  }'
```

#### Request URL

`https://api.tako.so/v2/lens/open_curation/curator/last_bid_price`

### Response

```
{
  "status": "success",
  "data": {
    "data": {
      "180": {
        "last_bid_price": "161000000000000"
      }
    }
  }
}
```
