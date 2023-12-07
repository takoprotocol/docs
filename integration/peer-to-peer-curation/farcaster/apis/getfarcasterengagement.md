# GetFarcasterEngagement

## API

<table><thead><tr><th width="168">API</th><th>/v2/farcaster/engagements</th></tr></thead><tbody><tr><td>Title</td><td>GetFarcasterEngagement</td></tr><tr><td>Description</td><td>Retrieve recent interaction data for certain profiles on Farcaster, such as the number of casts and replies sent. <br>Only publications initiated by these profiles will be counted.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="174">Name</th><th width="79">Type</th><th width="116">Required</th><th>Description</th></tr></thead><tbody><tr><td>fids</td><td>int[]</td><td>YES</td><td>The Farcaster FID list of the curators</td></tr><tr><td>interval</td><td>string</td><td>YES</td><td>“24h”, “3d”, “7d”, default to “24h”. <br>"24h" indicates 24 hours<br>"3d" indicates 3 days<br>"7d" indicates 7 days<br>Specify a time period and only analyze the activity data on Farcaster during that time.</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/farcaster/engagements' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "fids": [
      15706
    ],
    "interval": "7d"
  }'
```

#### Request URL

`https://api.tako.so/v2/farcaster/engagements`

### Response

```json
{
  "status": "success",
  "data": {
    "data": {
      "15706": {
        "cast": 0,
        "comment": 1,
        "like": 0,
        "link": 0,
        "mention": 0,
        "recast": 0
      }
    }
  }
}
```
