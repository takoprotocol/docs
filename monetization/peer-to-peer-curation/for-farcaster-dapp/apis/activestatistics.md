# ActiveStatistics

## API

<table><thead><tr><th width="174">API</th><th>/v2/{ecosystem}/active_statistics</th></tr></thead><tbody><tr><td>Title</td><td>LensActiveStatistics</td></tr><tr><td>Description</td><td>Retrieve recent interaction data for certain profiles on Lens or Farcaster, such as the number of followers, the number of comments received, and so on. <br>Only comments, mirrors, replies, or any other interaction from others on the posts made by these profiles will be counted. Posts initiated by these profiles will not be counted.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<mark style="color:red;">At least one of the profileIds and fids needs to be provided.</mark>

<mark style="color:red;">Provide fids when ecosystem is farcaster, and provide profileIds when ecosystem is lens</mark>

<table><thead><tr><th width="146">Name</th><th width="104">Type</th><th width="114">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YES</td><td>"lens" or "farcaster"</td></tr><tr><td>profileIds</td><td>uint[]</td><td>NO</td><td>The Lens profile id list of bidders or curators</td></tr><tr><td>fids</td><td>uint[]</td><td>NO</td><td>The Farcaster FID list of bidders or curators</td></tr><tr><td>interval</td><td>string</td><td>YES</td><td>“24h”, “3d”, “7d”, default to “24h”. <br>"24h" indicates 24 hours<br>"3d" indicates 3 days<br>"7d" indicates 7 days<br>Specify a time period and only analyze the activity data on Lens during that time.</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.tako.so/v2/lens/active_statistics' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "profileIds": [
      36112
    ],
    "interval": "7d"
  }'
```

#### Request URL

`https://api.tako.so/v2/lens/active_statistics`

### Response

```json
{
  "status": "success",
  "data": {
    "data": {
      "36112": {
        "comment": 0,
        "follow": 0,
        "mirror": 5
      }
    }
  }
}
```
