# verifyOpenCurationBid

## API

<table><thead><tr><th width="160">API</th><th>/v2/lens/open_curation/verify_bid</th></tr></thead><tbody><tr><td>Title</td><td>verifyOpenCurationBid</td></tr><tr><td>Description</td><td>Verify if the curator's task is completed and the curation has the best effect. The evaluation criteria for the effect are the highest sum of mirror and comment quantities in the curation quotes.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="168">Name</th><th width="111">Type</th><th width="121">Required</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>string</td><td>YES</td><td>The curator’s EVM-compatible address</td></tr><tr><td>index</td><td>int</td><td>NO</td><td>The index of bid</td></tr><tr><td>pubId</td><td>string</td><td>YES</td><td>The id of publication created by the curator</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/open_curation/verify_bid' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "address": "0x0f9Ab2e48665487BE9e2f5EF238496Ef9213AE57",
    "index": 17,
    "pubId": "0xb4-0x08-DA-67cfa258"
  }'
```

#### Request URL

`https://api.tako.so/v2/lens/open_curation/verify_bid`

### Response

<mark style="color:red;">When calling the</mark> `loanWithSig` <mark style="color:red;">method in the contract, you need to pass the</mark> `signature` <mark style="color:red;">and</mark> `relayer` <mark style="color:red;">from the response as parameters to</mark> `loanWithSig`<mark style="color:red;">. Please refer to the contract method for specific details.</mark>

<mark style="color:red;">The</mark> `loanWithSig` <mark style="color:red;">method in the contract is used to allow a curator to claim their reward when their curation is evaluated as the best after the curation is completed.</mark>

```
{
  "status": "success",
  "data": {
    "chainId": 80001,
    "contract": "0xC158A4319BC125e315120DbDfBEa8b8343aa3234",
    "curateDuration": 700,
    "relayer": "0x197309df1f580884B5A2A75DFd842a524Fd8AC15",
    "signature": {
      "r": "0xad8ff6eb40cb644715f3d662f994064920a2671d07507cff0307b0fd1980cfd0",
      "s": "0x733e7370a5ac2a4ce154e0be21a7cfe9a9460da737f30a007529ed0c9847cfaf",
      "v": 27,
      "deadline": 1700744961
    }
  }
}
```
