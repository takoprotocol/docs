# LensSearch

## API

<table><thead><tr><th width="169">API</th><th>/v1/lens/search</th></tr></thead><tbody><tr><td>Title</td><td>LensSearch</td></tr><tr><td>Description</td><td>Search the curators according to Lens handle or Lens profile id</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>keyword</td><td>string</td><td>YES</td><td>Lens handle or Lens profile id, such as curator.lens, 36112, etc</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.takoyaki.so/v1/lens/search?keyword=curator'
```

#### Request URL

`https://api.takoyaki.so/v1/lens/search?keyword=curator`

### Response

```json
{
  "status": "success",
  "data": {
    "items": [
      {
        "coverPicture": {
          "original": {
            "mimeType": "",
            "url": ""
          }
        },
        "dispatcher": {
          "address": "0x6C1e1bC39b13f9E0Af9424D76De899203F47755F"
        },
        "handle": "curator1.test",
        "lastAccept": {
          "price": 1000000000000,
          "token": "0x0000000000000000000000000000000000000000"
        },
        "ownedBy": "0x87A4798567135aD8fF1d380df18DBb63dD2771c8",
        "picture": {
          "original": {
            "mimeType": "",
            "url": ""
          }
        },
        "profileId": "0x8d11",
        "stats": {
          "totalCollects": 0,
          "totalComments": 0,
          "totalFollowers": 0,
          "totalFollowing": 0,
          "totalMirrors": 1,
          "totalPosts": 0,
          "totalPublications": 1
        }
      }
    ],
    "pageInfo": {
      "next": "{\"offset\":1}",
      "prev": "{\"offset\":0}",
      "totalCount": 1
    }
  }
}
```
