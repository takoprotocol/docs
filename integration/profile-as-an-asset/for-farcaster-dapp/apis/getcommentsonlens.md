# GetCommentsOnLens

## API

<table><thead><tr><th width="169">API</th><th>/token/profile/v1/content/lens/{id}/comments</th></tr></thead><tbody><tr><td>Title</td><td>GetCommentsOnLens</td></tr><tr><td>Description</td><td>Get comments of one publication on Lens</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="178">Name</th><th width="99">Type</th><th width="113">Required</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>YES</td><td>The id of publiaction</td></tr><tr><td>cursor</td><td>string</td><td>NO</td><td>After calling this API, you will get the parameter cursor from the return value. When calling this API again, pass cursor as the value for the parameter cursor, which filters out data before the cursor and only queries data after the cursor</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/token/profile/v1/content/lens/0x01-0x01/comments' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/token/profile/v1/content/lens/0x01-0x01/comments`

### Response

```json
{
  "code": 0,
  "msg": "OK",
  "data": {
    "trades": {},
    "items": [
      {
        "id": "0x56-0x06",
        "by": {
          "id": "0x56",
          "handle": {
            "fullHandle": "test/krzysu",
            "localName": "krzysu",
            "suggestedFormatted": {
              "localName": "@krzysu"
            },
            "linkedTo": {
              "nftTokenId": "0x56",
              "__typename": "HandleLinkedTo"
            }
          },
          "ownedBy": {
            "address": "0x3fC47cdDcFd59dce20694b575AFc1D94186775b0",
            "chainId": 80001
          },
          "metadata": {
            "displayName": "",
            "bio": "",
            "rawURI": "",
            "appId": null,
            "picture": {
              "optimized": {
                "uri": ""
              }
            }
          }
        },
        "createdAt": "2023-12-08T14:50:34Z",
        "stats": {
          "id": "0x56-0x06",
          "comments": 0,
          "mirrors": 0,
          "quotes": 0,
          "reactions": 0,
          "countOpenActions": 0,
          "bookmarks": 0
        },
        "operations": {
          "__typename": "PublicationOperations",
          "canComment": "NO",
          "canMirror": "NO",
          "hasActed": {
            "__typename": "OptimisticStatusResult",
            "value": false
          },
          "hasBookmarked": false,
          "hasMirrored": false,
          "hasQuoted": false,
          "hasReacted": false,
          "isNotInterested": false
        },
        "metadata": {
          "__typename": "TextOnlyMetadataV3",
          "appId": "hey",
          "attributes": null,
          "content": "hello",
          "id": "deec5a3e-a8bd-4c48-af4e-2e91921d95b9",
          "locale": "en",
          "rawURI": "ar://sNp8CX8u-gSl7kZ4mm-1Wv1Im8lQucMHs2_YKBT1rY8",
          "tags": null
        },
        "__typename": "Comment",
        "commentOn": {
          "__typename": "Post",
          "by": {
            "__typename": "Profile",
            "handle": {
              "__typename": "HandleInfo",
              "fullHandle": "test/lensprotocol",
              "linkedTo": {
                "__typename": "HandleLinkedTo",
                "nftTokenId": "0x01"
              },
              "localName": "lensprotocol",
              "suggestedFormatted": {
                "__typename": "SuggestedFormattedHandle",
                "localName": "@lensprotocol"
              }
            },
            "id": "0x01",
            "metadata": null,
            "ownedBy": {
              "__typename": "NetworkAddress",
              "address": "0x1A1cDf59C94a682a067fA2D288C2167a8506abd7",
              "chainId": 80001
            }
          },
          "createdAt": "2023-11-23T17:13:55.000Z",
          "id": "0x01-0x01",
          "isEncrypted": false,
          "isHidden": false,
          "metadata": {
            "__typename": "ImageMetadataV3",
            "appId": "hey",
            "asset": {
              "__typename": "PublicationMetadataMediaImage",
              "image": {
                "__typename": "EncryptableImageSet",
                "optimized": {
                  "__typename": "Image",
                  "uri": "https://ik.imagekit.io/lens/media-snapshot/44fb2eb851646cfe82daff3bbcb38a278d5e5c03e21699fcf8d0eacd1bb04f17.png"
                },
                "raw": {
                  "__typename": "EncryptableImage",
                  "uri": "ipfs://bafybeihcijwrdix32s7sg4khf3jgfvtvhu3yxif5tkxqtvpyovedtew2du"
                }
              }
            },
            "attachments": [
              {
                "__typename": "PublicationMetadataMediaImage",
                "image": {
                  "__typename": "EncryptableImageSet",
                  "optimized": {
                    "__typename": "Image",
                    "uri": "https://ik.imagekit.io/lens/media-snapshot/44fb2eb851646cfe82daff3bbcb38a278d5e5c03e21699fcf8d0eacd1bb04f17.png"
                  },
                  "raw": {
                    "__typename": "EncryptableImage",
                    "uri": "ipfs://bafybeihcijwrdix32s7sg4khf3jgfvtvhu3yxif5tkxqtvpyovedtew2du"
                  }
                }
              }
            ],
            "attributes": null,
            "content": "Today, we proudly introduce ourselves as Avara. \n\nAvara is the home to some of the most innovative web3 brands: Aave, Lens Protocol, GHO, Sonar, and now Family, all building towards a people powered internet that benefits all.\n\nWe're thrilled to announce the acquisition of Family. With Family, led by Benji Taylor, we're reinforcing our commitment to making web3 accessible through world class product design.\n\nRead the genesis post, penned by @lens/stani.\nhttps://avara.xyz/blog/introducing-avara-and-announcing-acquisition-of-family",
            "id": "7e0994f0-b01b-41d4-b625-193133417dc0",
            "locale": "en",
            "rawURI": "ar://jFpc9bUyrlYhOOBN3KCIpuT3aAgm5WymRno8pe3BJzg",
            "tags": null,
            "title": "Post by @avara"
          },
          "momoka": null,
          "openActionModules": [
            {
              "__typename": "LegacyFeeCollectModuleSettings",
              "type": "LegacyFeeCollectModule"
            }
          ],
          "operations": {
            "__typename": "PublicationOperations",
            "canComment": "NO",
            "canMirror": "NO",
            "hasActed": {
              "__typename": "OptimisticStatusResult",
              "value": false
            },
            "hasBookmarked": false,
            "hasMirrored": false,
            "hasQuoted": false,
            "hasReacted": false,
            "isNotInterested": false
          },
          "profilesMentioned": [],
          "publishedOn": {
            "__typename": "App",
            "id": "hey"
          },
          "stats": {
            "__typename": "PublicationStats",
            "bookmarks": 0,
            "comments": 2,
            "countOpenActions": 0,
            "id": "0x01-0x01",
            "mirrors": 0,
            "quotes": 0,
            "reactions": 0
          },
          "txHash": "0x4790f4638c209f0fdc55e6ff86781a84ba6e9ea03a390adf110d5b4b4c5c7cd6"
        }
      }
    ],
    "pageInfo": {
      "next": "",
      "__typename": "PaginatedResultInfo"
    }
  },
  "ts": "2023-12-21 09:08:00.78385"
}
```
