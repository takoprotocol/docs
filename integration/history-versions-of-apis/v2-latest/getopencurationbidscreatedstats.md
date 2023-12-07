# getOpenCurationBidsCreatedStats

## API

<table><thead><tr><th width="169">API</th><th>/v2/lens/open_curation/get_bids_created/stats</th></tr></thead><tbody><tr><td>Title</td><td>getOpenCurationBidsCreatedStats</td></tr><tr><td>Description</td><td>Analyze the relevant data of bids created on Lens</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="176">Name</th><th width="101">Type</th><th width="106">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileIds</td><td>string[]</td><td>YES</td><td>The Lens profile id list of the bidders</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/open_curation/get_bids_created/stats' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "profileIds": [
      36112
    ]
  }'
```

#### Request URL

`https://api.tako.so/v2/lens/open_curation/get_bids_created/stats`

### Response

```
{
  "status": "success",
  "data": {
    "all": 3,
    "pending": 2,
    "pass": 1,
    "cancel": 0,
    "ignored": 0
  }
}
```
