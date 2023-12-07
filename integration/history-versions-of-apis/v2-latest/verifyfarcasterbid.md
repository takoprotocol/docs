# VerifyFarcasterBid

## API

<table><thead><tr><th width="160">API</th><th>/v2/farcaster/verify_bid</th></tr></thead><tbody><tr><td>Title</td><td>VerifyFarcasterBid</td></tr><tr><td>Description</td><td>It would be best to do extra work to verify whether the curate works are done. The curator can claim his reward from the booster bid after verification</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="168">Name</th><th width="111">Type</th><th width="121">Required</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>string</td><td>YES</td><td>The curator’s EVM-compatible address</td></tr><tr><td>index</td><td>int</td><td>NO</td><td>The index of bid</td></tr><tr><td>hash</td><td>string</td><td>YES</td><td>The hash of publication created by the curator</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/farcaster/verify_bid' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "address": "0x47fcef6259d058bab9389819e683a957ff89ad0a",
    "hash": "0xbc8a2256384c6e995611fa90ce8c664d40e5c5d4",
    "index": 6
  }'
```

#### Request URL

`https://api.tako.so/v2/farcaster/verify_bid`

### Response

<mark style="color:red;">When calling the</mark> `loanWithSig` <mark style="color:red;">method in the contract, you need to pass the</mark> `signature` <mark style="color:red;">and</mark> `relayer` <mark style="color:red;">from the response as parameters to</mark> `loanWithSig`<mark style="color:red;">. Please refer to the contract method for specific details.</mark>

<mark style="color:red;">The</mark> `loanWithSig` <mark style="color:red;">method in the contract is used to allow a curator to claim their reward when their curation is evaluated as the best after the curation is completed.</mark>

```json
{
  "status": "success",
  "data": {
    "chainId": 10,
    "contract": "0x833e2cf3d2759783f771e13a3951194d1a280547",
    "relayer": "0x96216849c49358B10257cb55b28eA603c874b05E",
    "signature": {
      "r": "0x7417cc59f0ccfba0243c0c5640bd31a812e2f4988097027af8253abf8628c4f4",
      "s": "0x61988da0222e4b8ccc5c8cb1d85620b44bac6b71f1ba2609dd6c9315468ad788",
      "v": 27,
      "deadline": 1697558403
    }
  }
}
```
