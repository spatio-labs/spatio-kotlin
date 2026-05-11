
# Note

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** | Stable provider id for the note. |  |
| **title** | **kotlin.String** |  |  |
| **content** | **kotlin.String** | Markdown body. The block tree at &#x60;/v1/notes/{id}/blocks&#x60; is the canonical structured representation; &#x60;content&#x60; is a flattened markdown view kept for clients that don&#39;t render blocks.  |  |
| **archived** | **kotlin.Boolean** |  |  |
| **createdAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **updatedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **provider** | **kotlin.String** | Registered provider id (e.g. &#x60;native-notes&#x60;). |  [optional] |
| **accountId** | **kotlin.String** | Connected-account row this note belongs to. |  [optional] |
| **ownerUserId** | **kotlin.String** | User id of the note&#39;s owner. Surfaced so the renderer can show \&quot;Shared with you\&quot; when &#x60;ownerUserId&#x60; differs from the viewer&#39;s id. Empty for non-native providers.  |  [optional] |
| **icon** | **kotlin.String** | Emoji or short string used as the note&#39;s icon. |  [optional] |
| **coverImage** | [**java.net.URI**](java.net.URI.md) | URL of the note&#39;s cover image. |  [optional] |
| **parentId** | **kotlin.String** | Parent note id when notes are nested. |  [optional] |
| **properties** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md) | Free-form provider-specific properties (tags, etc.). |  [optional] |
| **lastEditedBy** | **kotlin.String** | User id of the most recent editor. |  [optional] |



