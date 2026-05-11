
# Slide

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** |  |  |
| **presentationId** | **kotlin.String** |  |  |
| **title** | **kotlin.String** |  |  |
| **position** | **kotlin.Int** | Zero-based position within the presentation. |  |
| **createdAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **updatedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **provider** | **kotlin.String** |  |  [optional] |
| **accountId** | **kotlin.String** |  |  [optional] |
| **notes** | **kotlin.String** | Speaker notes. |  [optional] |
| **layout** | **kotlin.String** | Free-form layout id. Provider-specific (&#x60;title&#x60;, &#x60;two-column&#x60;, &#x60;image-left&#x60;, custom). Not enumerated to avoid forcing a breaking change every time a provider adds one.  |  [optional] |
| **backgroundColor** | **kotlin.String** |  |  [optional] |
| **backgroundImageUrl** | [**java.net.URI**](java.net.URI.md) |  |  [optional] |
| **textColor** | **kotlin.String** |  |  [optional] |
| **transition** | **kotlin.String** | Free-form transition id. |  [optional] |



