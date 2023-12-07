# GetPubIndexPairs

## API

<table><thead><tr><th width="168">API</th><th>/v1/pub_index/pairs</th></tr></thead><tbody><tr><td>Title</td><td>GetPubIndexPairs</td></tr><tr><td>Description</td><td>Get the publication id of curation and its index on Tako. It will be used in the API verifyLensBid.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="174">Name</th><th width="79">Type</th><th width="116">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileIds</td><td>int[]</td><td>YES</td><td>The Lens profile id list of the curators</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.takoyaki.so/v1/pub_index/pairs' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "profileIds": [
    36113
  ]
}'
```

#### Request URL

`https://api.takoyaki.so/v1/pub_index/pairs`

### Response

```json
{
  "status": "success",
  "data": {
    "36113": [
      {
        "index": 17,
        "pub_id": "0x8d11-0x01-DA-2e031960",
        "profile_id": 36113,
        "create_at": 1691045400,
        "update_at": 1691045416,
        "state": "Pass"
      }
    ]
  }
}
```
