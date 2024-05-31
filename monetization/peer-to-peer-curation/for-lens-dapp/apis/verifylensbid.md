# VerifyLensBid

## API

<table><thead><tr><th width="160">API</th><th>/v2/lens/verify_bid</th></tr></thead><tbody><tr><td>Title</td><td>VerifyLensBid</td></tr><tr><td>Description</td><td><p>Momoka is now running for Lens. The user’s publications are possibly sent to the Momoka system or Polygon (the old mechanism). So part of the publications are from the Momoka, and the others are from the Polygon. </p><p></p><p>The data on Momoka and Polygon is separate. So the users cannot comment or mirror using Polygon for the Momoka publications. </p><p></p><p>Suppose the booster wants the curator to comment on or mirror a Momoka publication. The comment or mirror result will be sent to Momoka after the curator accepts the bid. Because Lens does not allow users to comment or mirror Momoka publications using Polygon. </p><p></p><p>Tako will do all the curate works for curators, such as comment, mirror, etc. It will be straightforward if Tako does all the work using Polygon because they all happen in Polygon. But if Tako has to use Momoka, it won’t be easy because Momoka and Polygon are separate. </p><p></p><p>So it would be best to do extra work to verify whether the curate works are done. The curator can claim his reward from the booster bid after verification.</p></td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="168">Name</th><th width="111">Type</th><th width="121">Required</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>string</td><td>YES</td><td>The curator’s EVM-compatible address</td></tr><tr><td>index</td><td>int</td><td>NO</td><td>The index of bid</td></tr><tr><td>pubId</td><td>string</td><td>YES</td><td>The id of publication created by the curator</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/verify_bid' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "address": "0x87A4798567135aD8fF1d380df18DBb63dD2771c8",
    "index": 36,
    "pubId": "0x8d11-0x07-DA-912405d7"
  }'
```

#### Request URL

`https://api.tako.so/v2/lens/verify_bid`

### Response

<mark style="color:red;">When calling the</mark> `loanWithSig` <mark style="color:red;">method in the contract, you need to pass the</mark> `signature` <mark style="color:red;">and</mark> `relayer` <mark style="color:red;">from the response as parameters to</mark> `loanWithSig`<mark style="color:red;">. Please refer to the contract method for specific details.</mark>

<mark style="color:red;">The</mark> `loanWithSig` <mark style="color:red;">method in the contract is used to allow a curator to claim their reward when their curation is evaluated as the best after the curation is completed.</mark>

```json
{
  "status": "success",
  "data": {
    "chainId": 80001,
    "contract": "0x30daf74D17781f0C2aB19db687F14E3293B17E7e",
    "relayer": "0x197309df1f580884B5A2A75DFd842a524Fd8AC15",
    "signature": {
      "r": "0x7417cc59f0ccfba0243c0c5640bd31a812e2f4988097027af8253abf8628c4f4",
      "s": "0x61988da0222e4b8ccc5c8cb1d85620b44bac6b71f1ba2609dd6c9315468ad788",
      "v": 27,
      "deadline": 1697558403
    }
  }
}
```
