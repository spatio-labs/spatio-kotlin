
# BulkDeleteTasksRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **taskIds** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **accountIds** | **kotlin.collections.List&lt;kotlin.String&gt;** | Parallel slice with taskIds — accountIds[i] targets taskIds[i]. |  [optional] |
| **taskId** | **kotlin.String** | Singular fallback when only deleting one task. |  [optional] |
| **accountId** | **kotlin.String** |  |  [optional] |



