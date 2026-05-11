
# FederatedSearchRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **query** | **kotlin.String** |  |  |
| **platforms** | [**inline**](#kotlin.collections.List&lt;Platforms&gt;) | Subset to fan out to. Empty means all available platforms. |  [optional] |
| **limit** | **kotlin.Int** |  |  [optional] |
| **pageTokens** | **kotlin.collections.Map&lt;kotlin.String, kotlin.String&gt;** | Per-platform cursor for pagination. |  [optional] |
| **workspaceId** | **kotlin.String** |  |  [optional] |
| **organizationId** | **kotlin.String** |  |  [optional] |
| **includeShared** | **kotlin.Boolean** |  |  [optional] |
| **includeArchived** | **kotlin.Boolean** |  |  [optional] |


<a id="kotlin.collections.List<Platforms>"></a>
## Enum: platforms
| Name | Value |
| ---- | ----- |
| platforms | notes, tasks, mail, calendar, files |



