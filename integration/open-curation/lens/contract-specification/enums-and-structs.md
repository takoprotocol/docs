# Enums and Structs

## enum AuditStatus

<table><thead><tr><th width="193">Enum</th><th>Description</th></tr></thead><tbody><tr><td>Pending</td><td>The bid is currently being curated.</td></tr><tr><td><del>Refuse</del></td><td><del>The bid has been refused.</del>  <br>This field does not apply to Open Curation</td></tr><tr><td>Pass</td><td>The bid has concluded curation, and the curator with the best curation effect has already claimed the reward.</td></tr><tr><td>Cancel</td><td>The curate time for the bid has passed. And there are no curators curating for the bid</td></tr></tbody></table>

## struct BidData

<table><thead><tr><th width="198.33333333333331">Parameter</th><th width="121">Type</th><th>Description</th></tr></thead><tbody><tr><td>contentId</td><td>string</td><td>The id of original content</td></tr><tr><td>bidToken</td><td>address</td><td>The address of token. Default to 0x0000000000000000000000000000000000000000 , namely Matic</td></tr><tr><td>bidAmount</td><td>uint256</td><td>The amount of bidToken</td></tr></tbody></table>

## struct Content

<table><thead><tr><th width="198.33333333333331">Parameter</th><th width="121">Type</th><th>Description</th></tr></thead><tbody><tr><td>contentId</td><td>string</td><td>The id of original content</td></tr><tr><td>bidToken</td><td>address</td><td>Token address. Default to 0x0000000000000000000000000000000000000000 , namely Matic</td></tr><tr><td>bidAddress</td><td>address</td><td>The bid creator’s EVM-compatible address</td></tr><tr><td>bidAmount</td><td>uint256</td><td>The amount of bidToken</td></tr><tr><td>bidTime</td><td>uint256</td><td>The bid posted time</td></tr><tr><td>curatorId</td><td>uint256</td><td>The bid accepter(curator)’s Lens profile id</td></tr><tr><td>curatorContentId</td><td>uint256</td><td>The id of curated publication.</td></tr><tr><td>status</td><td>AuditState</td><td>The state of the bid. “Pending”, “Refuse”, “Pass”, “Cancel”</td></tr></tbody></table>
