
# CreateNoteRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **title** | **kotlin.String** |  |  |
| **content** | **kotlin.String** |  |  [optional] |
| **icon** | **kotlin.String** |  |  [optional] |
| **coverImage** | [**java.net.URI**](java.net.URI.md) |  |  [optional] |
| **parentId** | **kotlin.String** |  |  [optional] |
| **properties** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md) |  |  [optional] |
| **accountId** | **kotlin.String** | Optional override for the target connected account. May also be passed as a &#x60;?accountId&#x3D;&#x60; query param.  |  [optional] |
| **provider** | **kotlin.String** | Optional provider id (alternative to &#x60;accountId&#x60; when only one account exists for the provider). May also be passed as a &#x60;?provider&#x3D;&#x60; query param.  |  [optional] |



