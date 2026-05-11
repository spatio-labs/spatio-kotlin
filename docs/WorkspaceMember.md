
# WorkspaceMember

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** |  |  |
| **role** | [**inline**](#Role) |  |  |
| **joinedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **email** | **kotlin.String** |  |  [optional] |
| **name** | **kotlin.String** |  |  [optional] |
| **avatar** | [**java.net.URI**](java.net.URI.md) |  |  [optional] |
| **user** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md) |  |  [optional] |


<a id="Role"></a>
## Enum: role
| Name | Value |
| ---- | ----- |
| role | owner, admin, member, guest |



