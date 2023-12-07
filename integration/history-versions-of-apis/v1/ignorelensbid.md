# IgnoreLensBid

## API

<table><thead><tr><th width="161">API</th><th>/v1/ignore_lens_bid</th></tr></thead><tbody><tr><td>Title</td><td>IgnoreLensBid</td></tr><tr><td>Description</td><td>The curator can ignore some bids, which will not remove the bid data, just hidden.</td></tr><tr><td>Authorization</td><td>Required. Put a key-value pair in the request body, the key is Authorization, and the value is "Bearer {token}", Use the API GetToken to acquire the token. Please read the example below for more detail.</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="150">Name</th><th width="88">Type</th><th width="106">Required</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>int</td><td>YES</td><td>The index of bid</td></tr><tr><td>platformType</td><td>string</td><td>YES</td><td>"momoka" or "polygon". The mention of "momoka" indicate that the content will be curated on Momoka, while the mention of "polygon" indicate that the content will be curated on Polygon</td></tr><tr><td>profileIds</td><td>int[]</td><td>NO</td><td>The Lens profile id list of the curators</td></tr><tr><td>ignore</td><td>bool</td><td>NO</td><td>True indicate ignore</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.takoyaki.so/v1/ignore_lens_bid' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhZGRyZXNzIjoiMHg4N0E0Nzk4NTY3MTM1YUQ4ZkYxZDM4MGRmMThEQmI2M2REMjc3MWM4IiwidHlwZSI6InRva2VuIiwiZXhwIjoxNjkwOTc3MTA2fQ.oUIK9CLarLGRGlff08YufSiQxkZ3D-hhWREfhbVgEYE' \
  -d '{
  "ignore": true,
  "index": 70,
  "platformType": "polygon"
}'
```

#### Request URL

`https://api.takoyaki.so/v1/ignore_lens_bid`

### Response

```json
{
  "status":"success",
  "data":"update ignore info of 70 to true succeed"
}
```
