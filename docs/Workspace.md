
# Workspace

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** |  |  |
| **name** | **kotlin.String** |  |  |
| **slug** | **kotlin.String** |  |  |
| **description** | **kotlin.String** |  |  [optional] |
| **logoUrl** | **kotlin.String** |  |  [optional] |
| **organizationId** | **kotlin.String** |  |  [optional] |
| **organization** | [**WorkspaceOrganization**](WorkspaceOrganization.md) |  |  [optional] |
| **role** | **kotlin.String** | The caller&#39;s role in this workspace (&#x60;owner&#x60;, &#x60;admin&#x60;, &#x60;member&#x60;, &#x60;guest&#x60;). |  [optional] |
| **settings** | [**kotlin.Any**](.md) | Per-workspace settings. Currently emitted as either an object (&#x60;{language, timezone, ...}&#x60;) on &#x60;GET /v1/workspaces/{id}&#x60; or a JSON-encoded string on &#x60;GET /v1/organizations/{id}/workspaces&#x60;. Treat as opaque and parse defensively.  |  [optional] |
| **isDefault** | **kotlin.Boolean** |  |  [optional] |
| **memberCount** | **kotlin.Int** |  |  [optional] |
| **billingTier** | **kotlin.String** |  |  [optional] |
| **createdAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **updatedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |



