# GetFarcasterBidsCreatedStats

## API

<table><thead><tr><th width="169">API</th><th>/v2/farcaster/get_bids_created/stats</th></tr></thead><tbody><tr><td>Title</td><td>GetFarcasterBidsCreatedStats</td></tr><tr><td>Description</td><td>Analyze the relevant data of bids created on Farcaster</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="176">Name</th><th width="101">Type</th><th width="106">Required</th><th>Description</th></tr></thead><tbody><tr><td>fids</td><td>string[]</td><td>YES</td><td>The Farcaster FID list of the bidders</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/farcaster/get_bids_created/stats' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "Fids": [
      15706
    ]
  }'
```

#### Request URL

`https://api.tako.so/v2/farcaster/get_bids_created/stats`

### Response

```json
{
  "status": "success",
  "data": {
    "all": 9,
    "pending": 0,
    "pass": 3,
    "cancel": 6,
    "ignored": 0
  }
}
```
