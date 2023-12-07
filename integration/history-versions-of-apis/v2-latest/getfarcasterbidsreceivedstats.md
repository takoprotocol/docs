# GetFarcasterBidsReceivedStats

## API

<table><thead><tr><th width="169">API</th><th>/v2/farcaster/get_bids_received/stats</th></tr></thead><tbody><tr><td>Title</td><td>GetFarcasterBidsReceivedStats</td></tr><tr><td>Description</td><td>Analyze the relevant data of bids received on Farcaster</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="174">Name</th><th width="111">Type</th><th width="108">Required</th><th>Description</th></tr></thead><tbody><tr><td>fids</td><td>string[]</td><td>YES</td><td>The Farcaster FID list of the bidders</td></tr><tr><td>includeIgnore</td><td>bool</td><td>NO</td><td>Should ignored content be included. Default to true.</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/farcaster/get_bids_received/stats' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "Fids": [
      15706
    ],
    "includeIgnore": true
  }'
```

#### Request URL

`https://api.tako.so/v2/farcaster/get_bids_received/stats`

### Response

```json
{
  "status": "success",
  "data": {
    "all": 10,
    "pending": 1,
    "pass": 2,
    "cancel": 7,
    "ignored": 0
  }
}
```
