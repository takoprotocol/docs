# Enums and Structs

## enum EIP712Signature

Please read [https://eips.ethereum.org/EIPS/eip-712](https://eips.ethereum.org/EIPS/eip-712)

<table><thead><tr><th width="190">Enum</th><th>Description</th></tr></thead><tbody><tr><td>v</td><td>-</td></tr><tr><td>r</td><td>-</td></tr><tr><td>s</td><td>-</td></tr><tr><td>deadline</td><td>-</td></tr></tbody></table>

## enum AuditStatus

<table><thead><tr><th width="193">Enum</th><th>Description</th></tr></thead><tbody><tr><td>Pending</td><td>The bid is awaiting curator review</td></tr><tr><td>Refuse</td><td>The bid has been refused.</td></tr><tr><td>Pass</td><td>The curator accepted the bid. The transaction is succeed.</td></tr><tr><td>Cancel</td><td>The bid has been canceled.</td></tr></tbody></table>

## enum BidType

<table><thead><tr><th width="195">Enum</th><th>Description</th></tr></thead><tbody><tr><td>Post</td><td>After accepting the bid, the curator should post a new publication on Lens.</td></tr><tr><td>Comment</td><td>After accepting the bid, the curator should comment on the creator's publication on Lens.</td></tr><tr><td>Mirror</td><td>After accepting the bid, the curator should mirror the creator's publication on Lens.</td></tr></tbody></table>

## enum Platform

<table><thead><tr><th width="195">Enum</th><th>Description</th></tr></thead><tbody><tr><td>Polygon</td><td>The architecture based on Polygon</td></tr><tr><td>Momoka</td><td>The architecture based on Momoka</td></tr></tbody></table>

## struct MerkleVerifyData

<table><thead><tr><th width="195">Enum</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>The index of data</td></tr><tr><td>merkleProof</td><td>The merkle proof</td></tr></tbody></table>

## struct BidData

<table><thead><tr><th width="198.33333333333331">Parameter</th><th width="121">Type</th><th>Description</th></tr></thead><tbody><tr><td>contentURI</td><td>string</td><td>The URI for the publication used for bidding</td></tr><tr><td>profileIdPointed</td><td>uint256</td><td>Only for comment and mirror bid. The profile id to point the comment/mirror to</td></tr><tr><td>pubIdPointed</td><td>uint256</td><td>Only for comment and mirror bid. The publication ID to point the comment/mirror to</td></tr><tr><td>bidToken</td><td>address</td><td>The address of token. Default to 0x0000000000000000000000000000000000000000 , namely Matic</td></tr><tr><td>bidAmount</td><td>uint256</td><td>The amount of bidToken</td></tr><tr><td>duration</td><td>uint256</td><td>The valid duration of the bid, a UNIX timestamp</td></tr><tr><td>toCurators</td><td>uint256[]</td><td>The target curator’s Lens profile ids</td></tr></tbody></table>

## struct Content

<table><thead><tr><th width="198.33333333333331">Parameter</th><th width="121">Type</th><th>Description</th></tr></thead><tbody><tr><td>contentURI</td><td>string</td><td>Only for post, comment, and mirror bids. Because these bids will create new publications on Lens, the publications should be sent to storage such as Bundlr. Then you will get the content URI.</td></tr><tr><td>profileIdPointed</td><td>uint256</td><td>Only for comment and mirror bid. The profile id to point the comment/mirror to</td></tr><tr><td>pubIdPointed</td><td>uint256</td><td>Only for comment and mirror bid. The publication ID to point the comment/mirror to</td></tr><tr><td>bidToken</td><td>address</td><td>The address of token. Default to 0x0000000000000000000000000000000000000000 , namely Matic</td></tr><tr><td>bidAmount</td><td>uint256</td><td>The amount of bidToken</td></tr><tr><td>bidAddress</td><td>address</td><td>The bid creator’s EVM-compatible address</td></tr><tr><td>bidExpires</td><td>uint256</td><td>The valid duration of the bid, a UNIX timestamp</td></tr><tr><td>toCurators</td><td>uint256[]</td><td>The target curator’s Lens profile ids</td></tr><tr><td>curatorId</td><td>uint256</td><td>The bid accepter(curator)’s Lens profile id</td></tr><tr><td>curatorContentId</td><td>uint256</td><td>The id of curated publication.</td></tr><tr><td>status</td><td>AuditState</td><td>The state of the bid. “Pending”, “Refuse”, “Pass”, “Cancel”</td></tr><tr><td>bidType</td><td>bidType</td><td>The type of bid. “Post”, “Comment”, “Mirror”</td></tr></tbody></table>

## struct MomokaBidData

<table><thead><tr><th width="201.33333333333331">Parameter</th><th width="120">Type</th><th>Description</th></tr></thead><tbody><tr><td>contentURI</td><td>string</td><td>Only for post, comment, and mirror bids. Because these bids will create new publications on Lens, the publications should be sent to storage such as Bundlr. Then you will get the content URI.</td></tr><tr><td>mirror</td><td>string</td><td>The ID of the publication that will be mirrored</td></tr><tr><td>commentOn</td><td>string</td><td>The ID of the publication that will be commented</td></tr><tr><td>bidToken</td><td>address</td><td>The address of token. Default to 0x0000000000000000000000000000000000000000 , namely Matic</td></tr><tr><td>bidAmount</td><td>uint256</td><td>The amount of bidToken</td></tr><tr><td>duration</td><td>uint256</td><td>The valid duration of the bid, a UNIX timestamp</td></tr><tr><td>toCurators</td><td>uint256[]</td><td>The target curator’s Lens profile ids</td></tr></tbody></table>

## struct MomokaContent

<table><thead><tr><th width="205.33333333333331">Parameter</th><th width="130">Type</th><th>Description</th></tr></thead><tbody><tr><td>contentURI</td><td>string</td><td>Only for post, comment, and mirror bids. Because these bids will create new publications on Lens, the publications should be sent to storage such as Bundlr. Then you will get the content URI.</td></tr><tr><td>mirror</td><td>string</td><td>The ID of the publication that will be mirrored</td></tr><tr><td>commentOn</td><td>string</td><td>The ID of the publication that will be commented</td></tr><tr><td>bidToken</td><td>address</td><td>The address of token. Default to 0x0000000000000000000000000000000000000000 , namely Matic</td></tr><tr><td>bidAmount</td><td>uint256</td><td>The amount of bidToken</td></tr><tr><td>bidAddress</td><td>address</td><td>The bid creator’s EVM-compatible address</td></tr><tr><td>bidExpires</td><td>uint256</td><td>The valid duration of the bid, a UNIX timestamp</td></tr><tr><td>toCurators</td><td>uint256[]</td><td>The target curator’s Lens profile ids</td></tr><tr><td>curatorId</td><td>uint256</td><td>The bid accepter(curator)’s Lens profile id</td></tr><tr><td>curatorContentId</td><td>string</td><td>The id of curated publication.</td></tr><tr><td>status</td><td>AuditStatus</td><td>The state of the bid. “Pending”, “Refuse”, “Pass”, “Cancel”</td></tr><tr><td>bidType</td><td>BidType</td><td>The type of bid. “Post”, “Comment”, “Mirror”</td></tr></tbody></table>
