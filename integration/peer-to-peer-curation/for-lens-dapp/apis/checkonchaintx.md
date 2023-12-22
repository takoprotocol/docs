# CheckOnchainTX

## API

<table><thead><tr><th width="169">API</th><th>/v2/hashes/confirmed</th></tr></thead><tbody><tr><td>Title</td><td>CheckOnchainTX</td></tr><tr><td>Description</td><td>To check if some transactions have been confirmed on the blockchain</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>hashes</td><td>string[]</td><td>YES</td><td>Transaction hash list</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/hashes/confirmed' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "hashes": [
      "0x50f7c8ef2bc580f0a199209001a1bac63e0fec04938cd7cde1a5dd18f41498fe"
    ]
  }'
```

#### Request URL

`https://api.tako.so/v2/hashes/confirmed`

### Response

```json
{
  "status": "success",
  "data": {
    "0x50f7c8ef2bc580f0a199209001a1bac63e0fec04938cd7cde1a5dd18f41498fe": true
  }
}
```
