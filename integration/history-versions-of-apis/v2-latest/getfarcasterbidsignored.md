# GetFarcasterBidsIgnored

## API

<table><thead><tr><th width="171">API</th><th>/v2/farcaster/get_bids_ignored</th></tr></thead><tbody><tr><td>Title</td><td>GetFarcasterBidsIgnored</td></tr><tr><td>Description</td><td>Get the bids which ignored by the curator</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="139">Name</th><th width="115">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>fids</td><td>int[]</td><td>YES</td><td>The Farcaster FID list of the bidders</td></tr><tr><td>bidType</td><td>string[]</td><td>NO</td><td>"Casts", "Reply", "Recasts"<br>If the bidType is not included in the request parameters, all data will be queried.</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, offsett 5 means that the first 5 rows of the query result will be skipped.</td></tr><tr><td>sort</td><td>string</td><td>NO</td><td>Can sort by "bid_amount", "create_at", "update_at", default to "bid_amount"</td></tr><tr><td>sortType</td><td>string</td><td>NO</td><td>“desc” or “asc”, default to “desc”. Arrange in ascending or descending order.</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/farcaster/get_bids_ignored' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "Fids": [
   15706
  ],
  "bidType": [
    "Casts","Reply","Recasts"
  ],
  "limit": 5,
  "offset": 0,
  "sort": "create_at",
  "sortType": "desc"
}'
```

#### Request URL

`https://api.tako.so/v2/farcaster/get_bids_ignored`

### Response

```json
{
  "status": "success",
  "data": {
    "bids": [],
    "total": 0
  }
}
```
