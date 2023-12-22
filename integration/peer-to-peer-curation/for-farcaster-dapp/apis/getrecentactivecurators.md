# GetRecentActiveCurators

## API

<table><thead><tr><th width="170">API</th><th>/v2/{ecosystem}/recent/curators</th></tr></thead><tbody><tr><td>Title</td><td>GetRecentActiveCurators</td></tr><tr><td>Description</td><td>Retrieve the recent profiles that have received and accepted bids</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="148">Name</th><th width="97">Type</th><th width="114">Required</th><th>Description</th></tr></thead><tbody><tr><td>ecosystem</td><td>string</td><td>YES</td><td>"lens" or "farcaster"</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/v2/lens/recent/curators' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/v2/lens/recent/curators`

### Response

```json
{
  "status": "success",
  "data": [
    {
      "item": {
        "id": 40,
        "index": 0,
        "ignores": null,
        "platform_type": "",
        "content_uri": "",
        "bid_token": "",
        "bid_address": "",
        "bid_amount": "100000000000000",
        "bid_expires": 0,
        "to_profiles": null,
        "curator_profile_id": 34550,
        "curator_pub_id": "",
        "bid_type": "",
        "others": null,
        "events": null,
        "create_at": 0,
        "update_at": 1693559472
      },
      "profile": {
        "id": "0x86f6",
        "name": "sparks",
        "bio": "",
        "attributes": [
          {
            "displayType": null,
            "traitType": null,
            "key": "app",
            "value": "Lenster"
          }
        ],
        "followNftAddress": "0xDa9594313EA5e45cCE569DEb9C0845de463F83ad",
        "metadata": "https://arweave.net/9glSzgWC0uJYH8pAhKKSCZb70OP6vpL1cYSOCLTTiz4",
        "isDefault": false,
        "picture": {
          "__typename": "MediaSet",
          "original": {
            "mimeType": null,
            "url": "https://ik.imagekit.io/lens/media-snapshot/a2af6746a6b3db597ba37e29b198185f7cbb4a87aaabda0510a54e0bbbdd57e8.jpg"
          }
        },
        "handle": "sparks.test",
        "coverPicture": null,
        "ownedBy": "0x26994399D0b5298262959493FD8f903B40E7F65d",
        "dispatcher": {
          "address": "0x6C1e1bC39b13f9E0Af9424D76De899203F47755F"
        },
        "stats": {
          "totalFollowers": 1,
          "totalFollowing": 0,
          "totalPosts": 74,
          "totalComments": 21,
          "totalMirrors": 28,
          "totalPublications": 123,
          "totalCollects": 0
        },
        "followModule": null
      },
      "curator_info": {
        "last_bid_price": "100000000000000"
      }
    },
    {
      "item": {
        "id": 30,
        "index": 0,
        "ignores": null,
        "platform_type": "",
        "content_uri": "",
        "bid_token": "",
        "bid_address": "",
        "bid_amount": "1200000000000000",
        "bid_expires": 0,
        "to_profiles": null,
        "curator_profile_id": 36113,
        "curator_pub_id": "",
        "bid_type": "",
        "others": null,
        "events": null,
        "create_at": 0,
        "update_at": 1692948703
      },
      "profile": {
        "id": "0x8d11",
        "name": "",
        "bio": "",
        "attributes": [],
        "followNftAddress": null,
        "metadata": "",
        "isDefault": false,
        "picture": null,
        "handle": "curator1.test",
        "coverPicture": null,
        "ownedBy": "0x87A4798567135aD8fF1d380df18DBb63dD2771c8",
        "dispatcher": {
          "address": ""
        },
        "stats": {
          "totalFollowers": 0,
          "totalFollowing": 0,
          "totalPosts": 2,
          "totalComments": 0,
          "totalMirrors": 6,
          "totalPublications": 8,
          "totalCollects": 0
        },
        "followModule": null
      },
      "curator_info": {
        "last_bid_price": "1200000000000000"
      }
    },
    {
      "item": {
        "id": 12,
        "index": 0,
        "ignores": null,
        "platform_type": "",
        "content_uri": "",
        "bid_token": "",
        "bid_address": "",
        "bid_amount": "0",
        "bid_expires": 0,
        "to_profiles": null,
        "curator_profile_id": 35463,
        "curator_pub_id": "",
        "bid_type": "",
        "others": null,
        "events": null,
        "create_at": 0,
        "update_at": 1692869635
      },
      "profile": {
        "id": "0x8a87",
        "name": "Angela",
        "bio": "Aw",
        "attributes": [],
        "followNftAddress": "0xC0996FB9F5B1306A36400005E6DC06428B54F6ab",
        "metadata": "https://arweave.net/LDwPgZXtg1kXZYa8LnWsX1Z7d2yLqMnD-7s6iQVGL2c",
        "isDefault": false,
        "picture": {
          "__typename": "MediaSet",
          "original": {
            "mimeType": null,
            "url": "https://ik.imagekit.io/lens/media-snapshot/bc9da677d0e35af515d8d4b558ac75cd5786444ef355c624003441d1e01d8354.png"
          }
        },
        "handle": "angelaa.test",
        "coverPicture": null,
        "ownedBy": "0xB6110344798b08f2bBC3FF82d0BA094e38D50f7f",
        "dispatcher": {
          "address": ""
        },
        "stats": {
          "totalFollowers": 0,
          "totalFollowing": 0,
          "totalPosts": 3,
          "totalComments": 2,
          "totalMirrors": 1,
          "totalPublications": 6,
          "totalCollects": 1
        },
        "followModule": null
      },
      "curator_info": {
        "last_bid_price": "0"
      }
    },
    {
      "item": {
        "id": 4,
        "index": 0,
        "ignores": null,
        "platform_type": "",
        "content_uri": "",
        "bid_token": "",
        "bid_address": "",
        "bid_amount": "20000000000000000",
        "bid_expires": 0,
        "to_profiles": null,
        "curator_profile_id": 34370,
        "curator_pub_id": "",
        "bid_type": "",
        "others": null,
        "events": null,
        "create_at": 0,
        "update_at": 1692867175
      },
      "profile": {
        "id": "0x8642",
        "name": "",
        "bio": "",
        "attributes": [],
        "followNftAddress": "0x035E2b571d98Ef238fD8C12D263B6f1726317a0b",
        "metadata": "",
        "isDefault": false,
        "picture": null,
        "handle": "lenstest1111.test",
        "coverPicture": null,
        "ownedBy": "0x793eC059cCc2Ceeb8c6748111550b23c4e0072Bb",
        "dispatcher": {
          "address": "0x6C1e1bC39b13f9E0Af9424D76De899203F47755F"
        },
        "stats": {
          "totalFollowers": 1,
          "totalFollowing": 0,
          "totalPosts": 27,
          "totalComments": 9,
          "totalMirrors": 31,
          "totalPublications": 67,
          "totalCollects": 0
        },
        "followModule": null
      },
      "curator_info": {
        "last_bid_price": "20000000000000000"
      }
    }
  ]
}
```
