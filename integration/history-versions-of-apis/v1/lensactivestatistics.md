# LensActiveStatistics

## API

<table><thead><tr><th width="174">API</th><th>/v1/lens_active_statistics</th></tr></thead><tbody><tr><td>Title</td><td>LensActiveStatistics</td></tr><tr><td>Description</td><td>View the recent activity data for a list of specified Lens profile id list on Lens.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="129">Name</th><th width="104">Type</th><th width="114">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileIds</td><td>string[]</td><td>YES</td><td>The lens profile id list of bidders or curators</td></tr><tr><td>interval</td><td>string</td><td>YES</td><td>“24h”, “3d”, “7d”, default to “24h”. <br>"24h" indicates 24 hours<br>"3d" indicates 3 days<br>"7d" indicates 7 days<br>Specify a time period and only analyze the activity data on Lens during that time.</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.takoyaki.so/v1/lens_active_statistics' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "interval": "24h",
  "profileIds": [
    36112
  ]
}'
```

#### Request URL

`https://api.takoyaki.so/v1/lens_active_statistics`

### Response

```json
{
  "status": "success",
  "data": {
    "data": {
      "36112": {
        "comment": 0,
        "follow": 0,
        "mirror": 0
      }
    }
  }
}
```
