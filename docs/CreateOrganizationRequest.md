
# CreateOrganizationRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **name** | **kotlin.String** |  |  |
| **slug** | **kotlin.String** | Auto-generated from &#x60;name&#x60; if omitted. Slug collisions are auto-suffixed with &#x60;-2&#x60;, &#x60;-3&#x60;, etc.  |  [optional] |
| **description** | **kotlin.String** |  |  [optional] |
| **logoUrl** | [**java.net.URI**](java.net.URI.md) |  |  [optional] |
| **createDefaultWorkspace** | **kotlin.Boolean** | &#x60;true&#x60; (default) creates a default workspace alongside the org. |  [optional] |
| **defaultWorkspaceName** | **kotlin.String** |  |  [optional] |



