
# FederatedSearch200Response

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **items** | [**kotlin.collections.List&lt;FederatedSearch200ResponseItemsInner&gt;**](FederatedSearch200ResponseItemsInner.md) |  |  |
| **perPlatform** | [**kotlin.collections.Map&lt;kotlin.String, FederatedSearch200ResponsePerPlatformValue&gt;**](FederatedSearch200ResponsePerPlatformValue.md) |  |  |
| **totalReturned** | **kotlin.Int** |  |  |
| **took** | **kotlin.String** | Aggregate wall-clock time for the fan-out, e.g. \&quot;120ms\&quot;. |  |
| **nextPageTokens** | **kotlin.collections.Map&lt;kotlin.String, kotlin.String&gt;** |  |  [optional] |
| **errors** | **kotlin.collections.Map&lt;kotlin.String, kotlin.String&gt;** | Per-platform errors. Other platforms still return results. |  [optional] |



