# View Functions

## getMinBidAmount

Retrieve the minimum bid token amount accepted by the curator.

`function getMinBidAmount(address wallet, address token) external view returns (uint256)`

<table><thead><tr><th width="148.33333333333331">Parameterss</th><th width="103">Type</th><th>Description</th></tr></thead><tbody><tr><td>wallet</td><td>address</td><td>An EVM-compatible address, namely Tako account</td></tr><tr><td>token</td><td>address</td><td>The accepted token address</td></tr></tbody></table>

## getDisableAcceptType

Retrieve whether the curator accepts a certain bidType.

`function getDisableAcceptType(address wallet, BidType bidType) external view returns (bool)`

<table><thead><tr><th width="150.33333333333331">Parameters</th><th width="107">Type</th><th>Description</th></tr></thead><tbody><tr><td>wallet</td><td>address</td><td>An EVM-compatible address, namely Tako account</td></tr><tr><td>bidType</td><td>BidType</td><td>Go to the page “Enums and Functions” for more details</td></tr></tbody></table>

## isBidTokenWhitelisted

Check whether the token accepts a certain bidType.

`function isBidTokenWhitelisted(address token) external view returns (bool)`

<table><thead><tr><th width="157.33333333333331">Parameters</th><th width="106">Type</th><th>Description</th></tr></thead><tbody><tr><td>token</td><td>address</td><td>The contract address of the token</td></tr></tbody></table>

## isRelayerWhitelisted

`function isRelayerWhitelisted(address wallet) external view returns (bool)`

<table><thead><tr><th width="157.33333333333331">Parameters</th><th width="106">Type</th><th>Description</th></tr></thead><tbody><tr><td>wallet</td><td>address</td><td>The address of relayer</td></tr></tbody></table>

## isGovernance

Verify if the address has governance privileges

`function isGovernance(address wallet) external view returns (bool)`

<table><thead><tr><th width="157.33333333333331">Parameters</th><th width="106">Type</th><th>Description</th></tr></thead><tbody><tr><td>wallet</td><td>address</td><td>The address of governance</td></tr></tbody></table>

## getContentByIndex

Get bid content by bid index.

`function getContentByIndex(uint256 index) external view returns (Content memory)`

<table><thead><tr><th width="158.33333333333331">Parameters</th><th width="106">Type</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>uint256</td><td>The index of content</td></tr></tbody></table>

## getBidCounter

Get the quantity of the bid

`function getBidCounter() external view returns (uint256)`
