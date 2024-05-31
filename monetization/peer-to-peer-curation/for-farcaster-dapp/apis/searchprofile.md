# SearchProfile

## API

<table><thead><tr><th width="169">API</th><th>/v2/{ecosystem}/search</th></tr></thead><tbody><tr><td>Title</td><td>SearchProfile</td></tr><tr><td>Description</td><td>Search the profiles on the social graph according to Lens handle, Lens profile id, Farcaster FName, and Farcaster FID</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YES</td><td>"lens" or "farcaster"</td></tr><tr><td>keyword</td><td>string</td><td>YES</td><td> Lens handle, Lens profile id, Farcaster FName, and Farcaster FID, such as curator.lens, 36112, etc</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/v2/farcaster/search?keyword=tako' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/v2/lens/search?keyword=tako`

### Response

```json
{
  "status": "success",
  "data": {
    "items": [
      {
        "activeOnFcNetwork": false,
        "displayName": "haltakov.eth",
        "fid": 2382,
        "followerCount": 98,
        "followingCount": 58,
        "lastAccept": {
          "price": 0,
          "token": "0x0000000000000000000000000000000000000000"
        },
        "ownedBy": "0xaa66Ae4447EE6db27145FeF3d3Bd2F61e3a616Ee",
        "pfp": {
          "url": "https://i.imgur.com/sT1N1mj.jpg",
          "verified": false
        },
        "profile": {
          "bio": {
            "mentions": [],
            "text": "Used to make BMWs drive themselves. Now, I make web3 easier at Fr0ntierX"
          },
          "location": {
            "description": "",
            "placeId": ""
          }
        },
        "username": "vlad",
        "viewerContext": {
          "canSendDirectCasts": false,
          "followedBy": false,
          "following": false
        }
      },
      {
        "activeOnFcNetwork": false,
        "displayName": "Nikita",
        "fid": 5184,
        "followerCount": 39,
        "followingCount": 10,
        "lastAccept": {
          "price": 0,
          "token": "0x0000000000000000000000000000000000000000"
        },
        "ownedBy": "0xCD964730c1c94Bb2a098f328127e1A27acB7e49b",
        "pfp": {
          "url": "https://pbs.twimg.com/profile_images/1588990084400939008/KsJwJ7jm_400x400.png",
          "verified": false
        },
        "profile": {
          "bio": {
            "mentions": [],
            "text": "web3 brand designer at @ sauced.xyz  linktr.ee/pxrxnoid"
          },
          "location": {
            "description": "",
            "placeId": ""
          }
        },
        "username": "nikitakoshi",
        "viewerContext": {
          "canSendDirectCasts": false,
          "followedBy": false,
          "following": false
        }
      },
      {
        "activeOnFcNetwork": false,
        "displayName": "w i l l",
        "fid": 10271,
        "followerCount": 19,
        "followingCount": 57,
        "lastAccept": {
          "price": 0,
          "token": "0x0000000000000000000000000000000000000000"
        },
        "ownedBy": "0x303CC3F9192b474530D6e33aBcd6184eacF6E716",
        "pfp": {
          "url": "https://i.imgur.com/3cwEfBw.jpg",
          "verified": false
        },
        "profile": {
          "bio": {
            "mentions": [],
            "text": ""
          },
          "location": {
            "description": "",
            "placeId": ""
          }
        },
        "username": "metakosmia",
        "viewerContext": {
          "canSendDirectCasts": false,
          "followedBy": false,
          "following": false
        }
      },
      {
        "activeOnFcNetwork": false,
        "displayName": "Tako Protocol ",
        "fid": 13475,
        "followerCount": 92,
        "followingCount": 13,
        "lastAccept": {
          "price": 0,
          "token": "0x0000000000000000000000000000000000000000"
        },
        "ownedBy": "0x851a87CaAF75024FDF4AEb05553fEd48b033F9fE",
        "pfp": {
          "url": "https://i.imgur.com/0XaYzjI.jpg",
          "verified": false
        },
        "profile": {
          "bio": {
            "mentions": [],
            "text": "Building The Open Social Recommendation Layer. \n\nRecommend, Advertise & Curate On Web3 Social.\n\nTako.so"
          },
          "location": {
            "description": "Singapore",
            "placeId": "ChIJyY4rtGcX2jERIKTarqz3AAQ"
          }
        },
        "username": "tako",
        "viewerContext": {
          "canSendDirectCasts": false,
          "followedBy": false,
          "following": false
        }
      }
    ]
  }
}
```
