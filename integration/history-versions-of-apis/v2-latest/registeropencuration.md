# registerOpenCuration

## API

<table><thead><tr><th width="160">API</th><th>/v2/lens/open_curation/register</th></tr></thead><tbody><tr><td>Title</td><td>registerOpenCuration</td></tr><tr><td>Description</td><td>After the curators complete the curation(i.e., quote the target publication on Lens), they must bind the Quoted Publication Id and Bid Index.<br>So that Tako can verify that the curators have completed the curation task.<br>This method is used to perform the binding.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="113">Name</th><th width="82">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>int</td><td>NO</td><td>The index of bid</td></tr><tr><td>pubId</td><td>string</td><td>NO</td><td>The id of Quoted Publication, such as 0x8d11-0x07-DA-1cdac4db</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/open_curation/register' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "index": 2,
    "pubId": "0x8d11-0x07-DA-1cdac4db"
  }'
```

#### Request URL

`https://api.tako.so/v2/lens/open_curation/register`

### Response

```
{
  "status": "success",
  "data": "register lens curation succeed"
}
```
