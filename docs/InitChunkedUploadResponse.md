
# InitChunkedUploadResponse

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **sessionId** | **kotlin.String** |  |  |
| **blocksToUpload** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  |
| **blocksAlreadyExist** | **kotlin.collections.List&lt;kotlin.String&gt;** | Blocks the platform already has and the client can skip (content-addressed deduplication).  |  |
| **deduplicationPct** | **kotlin.Double** |  |  |
| **estimatedUploadSize** | **kotlin.Long** |  |  |



