
# ClientRegistrationRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **clientName** | **kotlin.String** |  |  |
| **redirectUris** | [**kotlin.collections.List&lt;java.net.URI&gt;**](java.net.URI.md) |  |  |
| **grantTypes** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **responseTypes** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **scope** | **kotlin.String** | Space-separated scope list. Defaults to &#x60;read:*&#x60;. |  [optional] |
| **tokenEndpointAuthMethod** | [**inline**](#TokenEndpointAuthMethod) |  |  [optional] |
| **clientUri** | [**java.net.URI**](java.net.URI.md) |  |  [optional] |
| **logoUri** | [**java.net.URI**](java.net.URI.md) |  |  [optional] |
| **policyUri** | [**java.net.URI**](java.net.URI.md) |  |  [optional] |
| **tosUri** | [**java.net.URI**](java.net.URI.md) |  |  [optional] |


<a id="TokenEndpointAuthMethod"></a>
## Enum: token_endpoint_auth_method
| Name | Value |
| ---- | ----- |
| tokenEndpointAuthMethod | none, client_secret_basic, client_secret_post |



