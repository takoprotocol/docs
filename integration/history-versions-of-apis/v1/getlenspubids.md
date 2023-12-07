# GetLensPubIds

## API

<table><thead><tr><th width="169">API</th><th>/v1/lens_pubid</th></tr></thead><tbody><tr><td>Title</td><td>GetLensPubIds</td></tr><tr><td>Description</td><td>Retrieve all matching complete Lens publication IDs based on the full or partial Lens publication ID provided.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>YES</td><td>The full or partial Lens publication ID, such as 0x86f6-0x04-DA-defa9a6f</td></tr><tr><td>pubType</td><td>string</td><td>NO</td><td>“post”, “mirror”, “comment”, default to “post”. Only retrieve data of the specified pubType.</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.takoyaki.so/v1/lens_pubid?id=0x8&pubType=comment'
```

#### Request URL

`https://api.takoyaki.so/v1/lens_pubid?id=0x8&pubType=comment`

### Response

```json
{
  "status": "success",
  "data": {
    "pubIds": [
      "0x8642-0x18-DA-6bb6ef57",
      "0x09ad-0x8d",
      "0x09ad-0x8b",
      "0x09ad-0x89",
      "0x8642-0x17",
      "0x86f6-0x1b",
      "0x8a15-0x02",
      "0x87a8-0x0e",
      "0x8a60-0x45",
      "0x8a60-0x44",
      "0x8a60-0x43",
      "0x09ad-0x87",
      "0x8c25-0x04",
      "0x86f6-0x12",
      "0x09ad-0x85",
      "0x09ad-0x82",
      "0x88cc-0x10",
      "0x8c68-0x10",
      "0x8c68-0x0f",
      "0x8a60-0x41"
    ]
  }
}
```
