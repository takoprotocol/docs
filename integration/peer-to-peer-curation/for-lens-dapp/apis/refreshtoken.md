# RefreshToken

## API

<table><thead><tr><th width="191">Property</th><th>Value</th></tr></thead><tbody><tr><td>API</td><td>/v2/refresh_token</td></tr><tr><td>Title</td><td>RefreshToken</td></tr><tr><td>Description</td><td>For refreshing token</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="155">Name</th><th width="104">Type</th><th width="106">Required</th><th>Description</th></tr></thead><tbody><tr><td>refresh_token</td><td>string</td><td>YES</td><td>You can acquire the refresh_token by the API GetToken.</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/refresh_token' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhZGRyZXNzIjoiMHg0REQzREI1ZDBCOWFBZjBCMGEyZkJEMzdhNDg5ZDJmMGUzRjIzNEE5IiwidHlwZSI6InJlZnJlc2hfdG9rZW4iLCJleHAiOjE2OTEwNDYyNDd9.ghFd7X-FHnYW16VWyi-75tzEh5L_r06vjAIo3kKcGKM"
  }'
```

#### Request URL

`https://api.tako.so/v2/refresh_token`

### Response

> NOTE: The token is the only credential to access APIs, so you must save it securely. Its validity period is `3600` seconds. You can use the refresh\_token to refresh the token. Its validity period is `86400` seconds.

```json
{
  "status": "success",
  "data": {
    "token_type": "Bearer",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhZGRyZXNzIjoiMHg0REQzREI1ZDBCOWFBZjBCMGEyZkJEMzdhNDg5ZDJmMGUzRjIzNEE5IiwidHlwZSI6InRva2VuIiwiZXhwIjoxNjkwOTYzNzQyfQ.p822O9AwphgUSftpUIswjNtW7BjW8CQQ3u1yydlyMGM",
    "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhZGRyZXNzIjoiMHg0REQzREI1ZDBCOWFBZjBCMGEyZkJEMzdhNDg5ZDJmMGUzRjIzNEE5IiwidHlwZSI6InJlZnJlc2hfdG9rZW4iLCJleHAiOjE2OTEwNDY1NDJ9.El2EHD_3PhK_3MGiE_bSxbW2IyTJHn3xe3B0rVGQbWs",
    "expires_in": 3600
  }
}
```
