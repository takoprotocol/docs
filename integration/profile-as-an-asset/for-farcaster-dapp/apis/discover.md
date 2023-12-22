# Discover

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/content/discover</th></tr></thead><tbody><tr><td>Title</td><td>Discover</td></tr><tr><td>Description</td><td>Get the posts feed of creators who have activated their Profile Key</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YES</td><td>"lens" or "farcaster"</td></tr><tr><td>limit</td><td>int</td><td>YES</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>offset</td><td>int</td><td>NO</td><td>Specify the number of rows to be skipped from the beginning of the query result. For example, offsett 5 means that the first 5 rows of the query result will be skipped.</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/token/profile/v1/content/discover?ecosystem=farcaster&limit=10' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/token/profile/v1/content/discover?ecosystem=farcaster&limit=10`

### Response

```json
{
  "code": 0,
  "msg": "OK",
  "data": {
    "items": [
      {
        "hash": "0x57f8c700986f2a0c7ddfc366c10de2a6b91b59d2",
        "threadHash": "0x57f8c700986f2a0c7ddfc366c10de2a6b91b59d2",
        "parentHash": "",
        "parentAuthor": null,
        "author": {
          "fid": 10001,
          "username": "demo1",
          "displayName": "demo1",
          "pfp": {
            "url": "https://demo.com/demo1.jpg",
            "verified": false
          },
          "profile": {
            "bio": {
              "text": "",
              "mentions": []
            },
            "location": {
              "placeId": "demo",
              "description": "demo"
            }
          },
          "followerCount": 16,
          "followingCount": 21,
          "activeOnFcNetwork": false,
          "referrerUsername": "",
          "viewerContext": {
            "following": false,
            "followedBy": false,
            "canSendDirectCasts": false,
            "hasUploadedInboxKeys": false
          },
          "extras": {
            "fid": 10001,
            "custodyAddress": "0xcb093137a3098dEbBCe9C5D416D9A257914d9754"
          }
        },
        "embeds": {
          "images": [
            {
              "type": "image",
              "url": "https://demo.com/demo1.jpeg",
              "sourceUrl": "https://demo.com/demo1.jpeg",
              "alt": "Cast image embed"
            }
          ],
          "processedCastText": ""
        },
        "text": "",
        "timestamp": 1703218178000,
        "replies": {
          "count": 0
        },
        "reactions": {
          "count": 0
        },
        "recasts": {
          "count": 0,
          "recasters": []
        },
        "watches": {
          "count": 0
        },
        "recast": false,
        "viewerContext": null
      },
      {
        "hash": "0xed814e2d4ac14336b5028cb57d039594760d1461",
        "threadHash": "0xed814e2d4ac14336b5028cb57d039594760d1461",
        "parentHash": "",
        "parentAuthor": null,
        "author": {
          "fid": 10002,
          "username": "demo2",
          "displayName": "demo2",
          "pfp": {
            "url": "https://demo.com/demo2.jpg",
            "verified": false
          },
          "profile": {
            "bio": {
              "text": "",
              "mentions": []
            },
            "location": {
              "placeId": "demo",
              "description": "demo"
            }
          },
          "followerCount": 22,
          "followingCount": 34,
          "activeOnFcNetwork": false,
          "referrerUsername": "",
          "viewerContext": {
            "following": false,
            "followedBy": false,
            "canSendDirectCasts": false,
            "hasUploadedInboxKeys": false
          },
          "extras": {
            "fid": 10002,
            "custodyAddress": "0x1E76aF80cc21e1E3cf8F7d3C170D585D265E0a89"
          }
        },
        "embeds": {
          "images": [
            {
              "type": "image",
              "url": "https://demo.com/demo2.jpeg",
              "sourceUrl": "https://demo.com/demo2.jpeg",
              "alt": "Cast image embed"
            }
          ],
          "processedCastText": ""
        },
        "text": "",
        "timestamp": 1703213404000,
        "replies": {
          "count": 1
        },
        "reactions": {
          "count": 1
        },
        "recasts": {
          "count": 0,
          "recasters": []
        },
        "watches": {
          "count": 0
        },
        "recast": false,
        "viewerContext": null
      },
      ...
    ]
  },
  "ts": "2023-12-22 04:18:10.45494"
}
```
