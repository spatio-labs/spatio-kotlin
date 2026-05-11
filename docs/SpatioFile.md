
# SpatioFile

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** |  |  |
| **name** | **kotlin.String** |  |  |
| **propertySize** | **kotlin.Long** | Bytes. |  |
| **mimeType** | **kotlin.String** |  |  |
| **storageType** | **kotlin.String** | Backing storage class — &#x60;r2&#x60;, &#x60;gdrive&#x60;, &#x60;dropbox&#x60;, etc. Provider-specific; treat as opaque.  |  |
| **createdAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **updatedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **provider** | **kotlin.String** |  |  [optional] |
| **accountId** | **kotlin.String** |  |  [optional] |
| **folderId** | **kotlin.String** |  |  [optional] |
| **downloadUrl** | [**java.net.URI**](java.net.URI.md) | Pre-signed download URL when one is cached on the row. Use &#x60;GET /v1/files/{id}/download&#x60; for a guaranteed-fresh URL — this field can lag past expiry.  |  [optional] |
| **metadata** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md) |  |  [optional] |



