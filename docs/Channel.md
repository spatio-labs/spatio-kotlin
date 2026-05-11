
# Channel

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** |  |  |
| **name** | **kotlin.String** |  |  |
| **type** | **kotlin.String** | Provider-specific. Common canonicals: &#x60;channel&#x60; and &#x60;private&#x60; (group channels), &#x60;im&#x60; (1:1 DM), &#x60;mpim&#x60; (group DM).  |  |
| **isMember** | **kotlin.Boolean** |  |  |
| **isArchived** | **kotlin.Boolean** |  |  |
| **provider** | **kotlin.String** | Registered provider id (e.g. &#x60;slack&#x60;, &#x60;native-chat&#x60;).  |  [optional] |
| **accountId** | **kotlin.String** |  |  [optional] |
| **description** | **kotlin.String** |  |  [optional] |
| **topic** | **kotlin.String** |  |  [optional] |
| **memberCount** | **kotlin.Int** |  |  [optional] |
| **createdAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |



