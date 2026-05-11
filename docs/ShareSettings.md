
# ShareSettings

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **isPublic** | **kotlin.Boolean** |  |  |
| **hasPassword** | **kotlin.Boolean** |  |  |
| **shareToken** | **kotlin.String** | Opaque token embedded in the public URL. Empty when &#x60;isPublic&#x60; is false.  |  [optional] |
| **shareUrl** | [**java.net.URI**](java.net.URI.md) | Fully-qualified public viewer URL. Computed server-side from &#x60;PUBLIC_VIEWER_BASE&#x60; (defaults to &#x60;https://spatio.app&#x60;) and the share token. Empty when the note is private.  |  [optional] |
| **passwordSetAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) | When the current password was set, if any. |  [optional] |



