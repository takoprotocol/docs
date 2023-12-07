# getOpenCurationIdIndexPairs

## API

<table><thead><tr><th width="168">API</th><th>/v2/lens/open_curation/id_index/pairs</th></tr></thead><tbody><tr><td>Title</td><td>getOpenCurationIdIndexPairs</td></tr><tr><td>Description</td><td>Retrieve the bid of the curation that has ended and is waiting for the curator to claim the reward</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="174">Name</th><th width="79">Type</th><th width="116">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileIds</td><td>int[]</td><td>YES</td><td>The profile id list of the curators</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/open_curation/id_index/pairs' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "profileIds": [
      36113
    ]
  }'
```

#### Request URL

`https://api.tako.so/v2/lens/open_curation/id_index/pairs`

### Response

```
{
  "status": "success",
  "data": {
    "36113": [
      {
        "index": 2,
        "pub_id": "0x8d11-0x07-DA-1cdac4db",
        "profile_id": 36113,
        "create_at": 1697100000,
        "update_at": 1697426749,
        "state": "Pending"
      }
    ]
  }
}
```
