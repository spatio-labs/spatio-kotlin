
# PublicInvitationPayload

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **kind** | [**inline**](#Kind) |  |  |
| **id** | **kotlin.String** |  |  |
| **email** | **kotlin.String** |  |  |
| **role** | **kotlin.String** |  |  |
| **status** | [**inline**](#Status) |  |  |
| **workspaceId** | **kotlin.String** |  |  [optional] |
| **organizationId** | **kotlin.String** |  |  [optional] |
| **expiresAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **createdAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **workspace** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md) |  |  [optional] |
| **organization** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md) |  |  [optional] |
| **invitedBy** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md) |  |  [optional] |


<a id="Kind"></a>
## Enum: kind
| Name | Value |
| ---- | ----- |
| kind | workspace, organization |


<a id="Status"></a>
## Enum: status
| Name | Value |
| ---- | ----- |
| status | pending, accepted, revoked, expired |



