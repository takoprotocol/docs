# GetCommentsOnFarcaster

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/content/farcaster/{id}/comments</th></tr></thead><tbody><tr><td>Title</td><td>GetCommentsOnFarcaster</td></tr><tr><td>Description</td><td>Get comments of one publication on Farcaster</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>YES</td><td>The hash of publiaction</td></tr><tr><td>cursor</td><td>string</td><td>NO</td><td>After calling this API, you will get the parameter cursor from the return value. When calling this API again, pass cursor as the value for the parameter cursor, which filters out data before the cursor and only queries data after the cursor</td></tr><tr><td>username</td><td>string</td><td>YES</td><td>The creator's username</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/token/profile/v1/content/farcaster/0x06f2925a58d0f9a5769436e8a48a25eff8237114/comments?limit=TwentyFive&username=dwr.eth' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/token/profile/v1/content/farcaster/0x06f2925a58d0f9a5769436e8a48a25eff8237114/comments?limit=TwentyFive&username=dwr.eth`

### Response

```json
{
  "code": 0,
  "msg": "OK",
  "data": {
    "trades": {},
    "items": [
      {
        "hash": "0x50c9887e246569b30b922ea3b8900b4f456eb314",
        "threadHash": "0x06f2925a58d0f9a5769436e8a48a25eff8237114",
        "parentHash": "0x06f2925a58d0f9a5769436e8a48a25eff8237114",
        "parentAuthor": {
          "fid": 3,
          "username": "dwr.eth",
          "displayName": "Dan Romero",
          "pfp": {
            "url": "",
            "verified": false
          },
          "profile": {
            "bio": {
              "text": "Working on Farcaster and Warpcast.",
              "mentions": []
            },
            "location": {
              "placeId": "ChIJE9on3F3HwoAR9AhGJW_fL-I",
              "description": "Los Angeles, CA, USA"
            }
          },
          "followerCount": 32717,
          "followingCount": 2721,
          "activeOnFcNetwork": true,
          "referrerUsername": "",
          "viewerContext": {
            "following": false,
            "followedBy": false,
            "canSendDirectCasts": false,
            "hasUploadedInboxKeys": false
          },
          "extras": null
        },
        "author": {
          "fid": 347,
          "username": "greg",
          "displayName": "Greg",
          "pfp": {
            "url": "https://i.seadn.io/gae/YsASemS2qwPJK2yI9fmN8HX1-DeIDy9EQxX4KsRk9rkniwn9A7xUyMu_vKR75Oxrs8QAKfIjqdmf6Aw9A9fsehJHWSz2LiNpnV_TPQ?w=500&auto=format",
            "verified": false
          },
          "profile": {
            "bio": {
              "text": "I like building apps on web3 protocols. DevRel @ ENS Labs. gregskril.com",
              "mentions": []
            },
            "location": {
              "placeId": "ChIJOwg_06VPwokRYv534QaPC8g",
              "description": "New York, NY, USA"
            }
          },
          "followerCount": 28958,
          "followingCount": 594,
          "activeOnFcNetwork": true,
          "referrerUsername": "",
          "viewerContext": {
            "following": false,
            "followedBy": false,
            "canSendDirectCasts": false,
            "hasUploadedInboxKeys": false
          },
          "extras": {
            "fid": 347,
            "custodyAddress": "0xB4F195e9A982C2bA58988Cb2132557378e9E6b08"
          }
        },
        "embeds": {
          "images": [
            {
              "type": "image",
              "url": "https://res.cloudinary.com/merkle-manufactory/image/fetch/c_fill,f_jpg/https://i.imgur.com/4yCohXZ.jpg",
              "sourceUrl": "https://i.imgur.com/4yCohXZ.jpg",
              "alt": "Cast image embed"
            }
          ]
        },
        "text": "",
        "timestamp": 1703107502000,
        "replies": {
          "count": 0
        },
        "reactions": {
          "count": 13
        },
        "recasts": {
          "count": 0,
          "recasters": []
        },
        "watches": {
          "count": 0
        },
        "recast": false,
        "viewerContext": {
          "reacted": false,
          "recast": false,
          "watched": false
        }
      },
      {
        "hash": "0xf6fbdd5ca66a4cb457a3ff2ac93dffea7e8624c2",
        "threadHash": "0x06f2925a58d0f9a5769436e8a48a25eff8237114",
        "parentHash": "0x06f2925a58d0f9a5769436e8a48a25eff8237114",
        "parentAuthor": {
          "fid": 3,
          "username": "dwr.eth",
          "displayName": "Dan Romero",
          "pfp": {
            "url": "",
            "verified": false
          },
          "profile": {
            "bio": {
              "text": "Working on Farcaster and Warpcast.",
              "mentions": []
            },
            "location": {
              "placeId": "ChIJE9on3F3HwoAR9AhGJW_fL-I",
              "description": "Los Angeles, CA, USA"
            }
          },
          "followerCount": 32717,
          "followingCount": 2721,
          "activeOnFcNetwork": true,
          "referrerUsername": "",
          "viewerContext": {
            "following": false,
            "followedBy": false,
            "canSendDirectCasts": false,
            "hasUploadedInboxKeys": false
          },
          "extras": null
        },
        "author": {
          "fid": 194,
          "username": "rish",
          "displayName": "rish",
          "pfp": {
            "url": "https://res.cloudinary.com/merkle-manufactory/image/fetch/c_fill,f_png,w_256/https://lh3.googleusercontent.com/MEaRCAMdER6MKcvmlfN1-0fVxOGz6w98R8CrP_Rpzse9KZudgn95frTd0L0ZViWVklBj9fuAcJuM6tt7P-BRN0ouAR87NpzZeh2DGw",
            "verified": false
          },
          "profile": {
            "bio": {
              "text": "@neynar 🪐 | nf.td/rish",
              "mentions": [
                "neynar"
              ]
            },
            "location": {
              "placeId": "",
              "description": ""
            }
          },
          "followerCount": 15496,
          "followingCount": 487,
          "activeOnFcNetwork": true,
          "referrerUsername": "",
          "viewerContext": {
            "following": false,
            "followedBy": false,
            "canSendDirectCasts": false,
            "hasUploadedInboxKeys": false
          },
          "extras": {
            "fid": 194,
            "custodyAddress": "0xB95dC10483bE18F7C69DDF78D4BAAfEcc01c5530"
          }
        },
        "embeds": null,
        "text": "\"farcaster boycott person\" is how I am going to refer to them from now on",
        "timestamp": 1703107380000,
        "replies": {
          "count": 0
        },
        "reactions": {
          "count": 6
        },
        "recasts": {
          "count": 0,
          "recasters": []
        },
        "watches": {
          "count": 0
        },
        "recast": false,
        "viewerContext": {
          "reacted": false,
          "recast": false,
          "watched": false
        }
      },
      {
        "hash": "0x42e190d86758c922c2535811850d42fd64f0ee18",
        "threadHash": "0x06f2925a58d0f9a5769436e8a48a25eff8237114",
        "parentHash": "0x06f2925a58d0f9a5769436e8a48a25eff8237114",
        "parentAuthor": {
          "fid": 3,
          "username": "dwr.eth",
          "displayName": "Dan Romero",
          "pfp": {
            "url": "",
            "verified": false
          },
          "profile": {
            "bio": {
              "text": "Working on Farcaster and Warpcast.",
              "mentions": []
            },
            "location": {
              "placeId": "ChIJE9on3F3HwoAR9AhGJW_fL-I",
              "description": "Los Angeles, CA, USA"
            }
          },
          "followerCount": 32717,
          "followingCount": 2721,
          "activeOnFcNetwork": true,
          "referrerUsername": "",
          "viewerContext": {
            "following": false,
            "followedBy": false,
            "canSendDirectCasts": false,
            "hasUploadedInboxKeys": false
          },
          "extras": null
        },
        "author": {
          "fid": 557,
          "username": "pugson",
          "displayName": "pugson",
          "pfp": {
            "url": "https://i.seadn.io/gae/5hjYfRyqiRJV4EQ7ieSJrmb1LtO_vcAvREXSqnlY4HXXBsvgh1vumOwj5e4GwGhppEU2jLC9qJHEgEkaJ9V_B02jIFY9XmzgK1_F?w=500&auto=format",
            "verified": false
          },
          "profile": {
            "bio": {
              "text": "✦ 𝚆𝙸𝙿: @vision 👁️ ✦ ensdata.net ✦ abidata.net ✦ 𝙿𝚁𝙴𝚅: ui engineer @rainbow  🌈  ✦ final-v3.zip",
              "mentions": [
                "vision",
                "rainbow"
              ]
            },
            "location": {
              "placeId": "",
              "description": ""
            }
          },
          "followerCount": 22008,
          "followingCount": 1619,
          "activeOnFcNetwork": true,
          "referrerUsername": "",
          "viewerContext": {
            "following": false,
            "followedBy": false,
            "canSendDirectCasts": false,
            "hasUploadedInboxKeys": false
          },
          "extras": {
            "fid": 557,
            "custodyAddress": "0xD7648B9d940e051b76Fc7d755138159E6cE2436E"
          }
        },
        "embeds": null,
        "text": "i'm offended that you're chatting over twitter dms",
        "timestamp": 1703113112000,
        "replies": {
          "count": 0
        },
        "reactions": {
          "count": 4
        },
        "recasts": {
          "count": 0,
          "recasters": []
        },
        "watches": {
          "count": 0
        },
        "recast": false,
        "viewerContext": {
          "reacted": false,
          "recast": false,
          "watched": false
        }
      },
      ...
    ],
    "pageInfo": {
      "cursor": ""
    }
  },
  "ts": "2023-12-21 08:23:26.24207"
}
```
