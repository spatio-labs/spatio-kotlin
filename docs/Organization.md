
# Organization

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** |  |  |
| **name** | **kotlin.String** |  |  |
| **slug** | **kotlin.String** |  |  |
| **role** | **kotlin.String** | The caller&#39;s role in this org (&#x60;owner&#x60;, &#x60;admin&#x60;, &#x60;billing_admin&#x60;, &#x60;member&#x60;). |  |
| **createdAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **updatedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **description** | **kotlin.String** |  |  [optional] |
| **logoUrl** | **kotlin.String** |  |  [optional] |
| **memberCount** | **kotlin.Int** |  |  [optional] |
| **workspaceCount** | **kotlin.Int** |  |  [optional] |
| **workspaces** | [**kotlin.collections.List&lt;OrganizationWorkspacesInner&gt;**](OrganizationWorkspacesInner.md) | Compact workspace summaries embedded in the org-list response. |  [optional] |



