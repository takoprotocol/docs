# GetToken

## API

<table><thead><tr><th width="167">Property</th><th>Value</th></tr></thead><tbody><tr><td>API</td><td>/v1/token</td></tr><tr><td>Title</td><td>GetToken</td></tr><tr><td>Description</td><td>Sign in Tako</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="119">Name</th><th width="86">Type</th><th width="72">Required</th><th>Description</th></tr></thead><tbody><tr><td>message</td><td>string</td><td>YES</td><td><p>Format: </p><p><mark style="color:red;"><code>\nACCOUNT:\n{EVM-compatible Address}\nISSUED AT:\n{Time in RFC3339 format}\n\n</code></mark></p><p></p><p>NOTE: The message structure above must be included, additional content can be added at the beginning and end of the message.</p><p></p><p>For example: </p><p><mark style="color:red;"><code>Tako wants you to sign in with your Ethereum account.\n\nThis request will not trigger a blockchain transaction or cost any gas fees.\n\nACCOUNT:\n0x4DD3DB5d0B9aAf0B0a2fBD37a489d2f0e3F234A9\n\nISSUED AT:\n2023-08-01T10:29:31.000Z\n</code></mark></p><p></p><p>What looks like on the user’s wallet signing page, such as Metamask: </p><p><mark style="color:red;"><code>Tako wants you to sign in with your Ethereum account.</code></mark></p><p></p><p><mark style="color:red;"><code>This request will not trigger a blockchain transaction or cost any gas fees.</code></mark></p><p></p><p><mark style="color:red;"><code>ACCOUNT:</code></mark></p><p><mark style="color:red;"><code>0x4DD3DB5d0B9aAf0B0a2fBD37a489d2f0e3F234A9</code></mark></p><p></p><p><mark style="color:red;"><code>ISSUED AT:</code></mark></p><p><mark style="color:red;"><code>2023-08-01T10:29:31.000Z</code></mark></p><p></p><p></p></td></tr><tr><td>signature</td><td>string</td><td>YES</td><td>Elliptic curve signing of the message.</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.takoyaki.so/v1/token' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "message": "Tako wants you to sign in with your Ethereum account.\n\nThis request will not trigger a blockchain transaction or cost any gas fees.\n\nACCOUNT:\n0x4DD3DB5d0B9aAf0B0a2fBD37a489d2f0e3F234A9\n\nISSUED AT:\n2023-08-01T10:29:31.000Z\n\n",
  "signature": "0xa480712751eea94815608cd58a153b6380608d2b79439d9033eb936f9a23ef8445c59b3f60f76b0b411e67798e0a3c92750fda60fc15699cf5f247d3f3435ce31b"
}'
```

#### Request URL

`https://api.takoyaki.so/v1/token`

### Response

> NOTE: The token is the only credential to access APIs, so you must save it securely. Its validity period is `3600` seconds. You can use the refresh\_token to refresh the token. Its validity period is `86400` seconds.

```json
{
  "status": "success",
  "data": {
    "token_type": "Bearer",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhZGRyZXNzIjoiMHg0REQzREI1ZDBCOWFBZjBCMGEyZkJEMzdhNDg5ZDJmMGUzRjIzNEE5IiwidHlwZSI6InRva2VuIiwiZXhwIjoxNjkwOTYzNDQ3fQ.VeRSLf-8sEb6nsdieGBuJI8wktCyJPKzTLx-opCX7x4",
    "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhZGRyZXNzIjoiMHg0REQzREI1ZDBCOWFBZjBCMGEyZkJEMzdhNDg5ZDJmMGUzRjIzNEE5IiwidHlwZSI6InJlZnJlc2hfdG9rZW4iLCJleHAiOjE2OTEwNDYyNDd9.ghFd7X-FHnYW16VWyi-75tzEh5L_r06vjAIo3kKcGKM",
    "expires_in": 3600
  }
}
```
