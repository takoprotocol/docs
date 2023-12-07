# GetFarcasterCuratorAccepted

## API

<table><thead><tr><th width="160">API</th><th>/v2/farcaster/curator/accepted</th></tr></thead><tbody><tr><td>Title</td><td>GetFarcasterCuratorAccepted</td></tr><tr><td>Description</td><td>Retrieve the last 10 completed bids</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>GET</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="113">Name</th><th width="82">Type</th><th width="110">Required</th><th>Description</th></tr></thead><tbody><tr><td>fid</td><td>string</td><td>NO</td><td>The Farcaster FID of curator</td></tr><tr><td>limit</td><td>int</td><td>NO</td><td>The number of bids displayed per page, default to 10</td></tr><tr><td>cursor</td><td>int</td><td>NO</td><td>The id of bid. After calling this API, you will get the parameter next_cursor from the return value. When calling this API again, pass next_cursor as the value for the parameter cursor, which filters out data before the cursor and only queries data after the cursor.</td></tr></tbody></table>

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'GET' \
  'https://api.tako.so/v2/farcaster/curator/accepted?fid=15706' \
  -H 'accept: application/json'
```

#### Request URL

`https://api.tako.so/v2/farcaster/curator/accepted?fid=15706`

### Response

```json
{
  "status": "success",
  "data": {
    "list": [
      {
        "id": 446,
        "index": 0,
        "content_uri": "ar://P8x2k5VFTvuSxc11fel6hNiHYDZz95OkaF9dZjVbWbs",
        "parent_hash": "",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0x47Fcef6259d058BaB9389819E683A957ff89AD0a",
        "bid_amount": "0",
        "curator_fid": 15706,
        "curator_hash": "0xc692b93c06651250b883519b11921a3a278cf8a5",
        "state": "",
        "bid_type": "Reply",
        "profile": {
          "fid": 15706,
          "username": "eekeekkeekeekko",
          "displayName": "Ekkooo",
          "pfp": {
            "url": "https://i.seadn.io/gae/4419AFbUnbFIlhdirdBDa5veEeb7c541FdtxkG5sKiC-YTU4FRegetJCwl8jWPG8Cc1J0y7OTg0zSx2pTENyi4_yDy6bmOjSnTLSjA?w=500&auto=format"
          }
        },
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0x96d4c25169c43c71a2e1c2dcf7ef561ae1ca24a5856ac9b37e7bf40382c76b7f",
            "event_name": "addBidEvent",
            "block_number": 109494366,
            "block_timestamp": 1694587509
          },
          "modifiBidEventPass": {
            "state": "Pass",
            "tx_hash": "0x12a5c0fbaf09387eca85de8d2901f91805964e219063184778222ef2ea7b3998",
            "event_name": "modifiBidEvent",
            "block_number": 109496714,
            "block_timestamp": 1694592205
          }
        },
        "create_at": 1694587509,
        "update_at": 1694592205
      },
      {
        "id": 120,
        "index": 0,
        "content_uri": "ar://O3FfX9dNftbtpEUZe34cByRqkavzDEMVb9n3Sf1bBSc",
        "parent_hash": "",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0x47Fcef6259d058BaB9389819E683A957ff89AD0a",
        "bid_amount": "0",
        "curator_fid": 15706,
        "curator_hash": "0xbc8a2256384c6e995611fa90ce8c664d40e5c5d4",
        "state": "",
        "bid_type": "Cast",
        "profile": {
          "fid": 15706,
          "username": "eekeekkeekeekko",
          "displayName": "Ekkooo",
          "pfp": {
            "url": "https://i.seadn.io/gae/4419AFbUnbFIlhdirdBDa5veEeb7c541FdtxkG5sKiC-YTU4FRegetJCwl8jWPG8Cc1J0y7OTg0zSx2pTENyi4_yDy6bmOjSnTLSjA?w=500&auto=format"
          }
        },
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0x5055ffe8a1731b0655836410f9f65f9ceaf79c8cdfb41f497f8100a47eba6f3f",
            "event_name": "addBidEvent",
            "block_number": 109493016,
            "block_timestamp": 1694584809
          },
          "modifiBidEventPass": {
            "state": "Pass",
            "tx_hash": "0x36154ea6091897900710d7c923ead21e8a2de6ee696863962d75cedf3203ecb3",
            "event_name": "modifiBidEvent",
            "block_number": 109494585,
            "block_timestamp": 1694587947
          },
          "modifiBidEventPending": {
            "state": "Pending",
            "tx_hash": "0x9f1fcab3b7dd3242d99508e6292802a83d1c8a5ec8447bf86430fcc1bf8ce162",
            "event_name": "modifiBidEvent",
            "block_number": 109493587,
            "block_timestamp": 1694585951
          }
        },
        "create_at": 1694584809,
        "update_at": 1694587947
      }
    ],
    "has_more": false,
    "next_cursor": 0
  }
}
```
