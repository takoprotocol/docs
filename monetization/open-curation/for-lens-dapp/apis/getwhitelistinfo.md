# GetWhitelistInfo

## API

<table><thead><tr><th width="191">Property</th><th>Value</th></tr></thead><tbody><tr><td>API</td><td>/v2/whitelist_info/{address}</td></tr><tr><td>Title</td><td>GetWhitelistInfo</td></tr><tr><td>Description</td><td>Retrieve whitelist information for a wallet address. The information needs to be passed when invoking the whitelist verification method of the contract.</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="155">Name</th><th width="104">Type</th><th width="106">Required</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>address</td><td>YES</td><td>An EVM-compatible address</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/v2/whitelist_info/0x0233eA33f8e68Cf7B631AA6dBb81df0058DB5783' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/v2/whitelist_info/0x0233eA33f8e68Cf7B631AA6dBb81df0058DB5783`

### Response

```json
{
  "status": "success",
  "data": {
    "address": "0x0233eA33f8e68Cf7B631AA6dBb81df0058DB5783",
    "merkleRoot": "0xb6cab120cfe96adedc28efe499f23e2289121e9558ea7755ddbc409768ff1ad4"
  }
}
```
