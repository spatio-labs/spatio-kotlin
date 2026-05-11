
# Recommendation

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** |  |  |
| **status** | [**inline**](#Status) |  |  |
| **workspaceId** | **kotlin.String** |  |  [optional] |
| **userId** | **kotlin.String** |  |  [optional] |
| **kind** | **kotlin.String** | Provider-tagged proposal kind (e.g. &#x60;note.draft&#x60;, &#x60;task.followup&#x60;). |  [optional] |
| **title** | **kotlin.String** |  |  [optional] |
| **body** | **kotlin.String** |  |  [optional] |
| **payload** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md) |  |  [optional] |
| **createdAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **updatedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **expiresAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |


<a id="Status"></a>
## Enum: status
| Name | Value |
| ---- | ----- |
| status | pending, accepted, dismissed, expired |



