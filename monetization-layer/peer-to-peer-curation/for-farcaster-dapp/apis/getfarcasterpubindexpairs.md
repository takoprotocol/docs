# GetFarcasterPubIndexPairs

## API

<table><thead><tr><th width="168">API</th><th>/v2/farcaster/id_index/pairs</th></tr></thead><tbody><tr><td>Title</td><td>GetFarcasterPubIndexPairs</td></tr><tr><td>Description</td><td>Retrieve the bid of the curation that has ended and is waiting for the curator to claim the reward</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="174">Name</th><th width="79">Type</th><th width="116">Required</th><th>Description</th></tr></thead><tbody><tr><td>fids</td><td>int[]</td><td>YES</td><td>The Farcaster FID list of the curators</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/farcaster/id_index/pairs' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "fids": [
      15706
    ]
  }'
```

#### Request URL

`https://api.tako.so/v2/farcaster/id_index/pairs`

### Response

```json
{
  "status": "success",
  "data": {
    "15706": [
      {
        "index": 6,
        "hash": "0xbc8a2256384c6e995611fa90ce8c664d40e5c5d4",
        "fid": 15706,
        "create_at": 1694587902,
        "update_at": 1694587939,
        "state": "Pass"
      },
      {
        "index": 8,
        "hash": "0x38e07f27f169c4125282c12364b64a47d00b673f",
        "fid": 15706,
        "create_at": 1694588919,
        "update_at": 1694588919,
        "state": "Pass"
      },
      {
        "index": 8,
        "hash": "0xc692b93c06651250b883519b11921a3a278cf8a5",
        "fid": 15706,
        "create_at": 1694592190,
        "update_at": 1694592196,
        "state": "Pass"
      },
      {
        "index": 21,
        "hash": "0x900d0a0878661d178a694eb5924629ead1ee9d6e",
        "fid": 15706,
        "create_at": 1694765390,
        "update_at": 1694765390,
        "state": "Pending"
      }
    ]
  }
}
```
