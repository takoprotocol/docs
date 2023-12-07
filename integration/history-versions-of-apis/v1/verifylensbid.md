# VerifyLensBid

## API

<table><thead><tr><th width="160">API</th><th>/v1/verify_lens_bid</th></tr></thead><tbody><tr><td>Title</td><td>VerifyLensBid</td></tr><tr><td>Description</td><td><p>Momoka is now running for Lens. The user’s publications are possibly sent to the Momoka system or Polygon (the old mechanism). So part of the publications are from the Momoka, and the others are from the Polygon. </p><p></p><p>The data on Momoka and Polygon is separate. So the users cannot comment or mirror using Polygon for the Momoka publications. </p><p></p><p>Suppose the booster wants the curator to comment on or mirror a Momoka publication. The comment or mirror result will be sent to Momoka after the curator accepts the bid. Because Lens does not allow users to comment or mirror Momoka publications using Polygon. </p><p></p><p>Tako will do all the curate works for curators, such as comment, mirror, etc. It will be straightforward if Tako does all the work using Polygon because they all happen in Polygon. But if Tako has to use Momoka, it won’t be easy because Momoka and Polygon are separate. </p><p></p><p>So it would be best to do extra work to verify whether the curate works are done. The curator can claim his reward from the booster bid after verification.</p></td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="168">Name</th><th width="111">Type</th><th width="121">Required</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>string</td><td>YES</td><td>The curator’s EVM-compatible address</td></tr><tr><td>index</td><td>int</td><td>NO</td><td>The index of bid</td></tr><tr><td>pubId</td><td>string</td><td>YES</td><td>The id of publication created by the curator</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.takoyaki.so/v1/verify_lens_bid' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "address": "0x87A4798567135aD8fF1d380df18DBb63dD2771c8",
  "index": 17,
  "pubId": "0x8d11-0x01-DA-2e031960"
}'
```

#### Request URL

`https://api.takoyaki.so/v1/verify_lens_bid`

### Response

```json
{
  "status": "success",
  "data": {
    "chainId": 80001,
    "contract": "0x7dff5E5B7bF2D3158B381Df56530cf80ef742aB8",
    "relayer": "0x197309df1f580884B5A2A75DFd842a524Fd8AC15",
    "signature": {
      "deadline": 1691082657,
      "r": "0xa68c4f487d21bf026e56be2e968dc367ebdafef4b6ee509a52af380d71b2dad2",
      "s": "0x617d3d46f677bd71ff9b19f8661347bb0c39b369be0911e3fc95d2fa07165b93",
      "v": 27
    }
  }
}
```
