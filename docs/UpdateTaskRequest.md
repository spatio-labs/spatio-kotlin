
# UpdateTaskRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **title** | **kotlin.String** |  |  [optional] |
| **description** | **kotlin.String** |  |  [optional] |
| **status** | **kotlin.String** |  |  [optional] |
| **dueDate** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **priority** | [**inline**](#Priority) |  |  [optional] |
| **labels** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **tags** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **assigneeId** | **kotlin.String** |  |  [optional] |
| **parentTaskId** | **kotlin.String** |  |  [optional] |


<a id="Priority"></a>
## Enum: priority
| Name | Value |
| ---- | ----- |
| priority | none, low, medium, high, urgent |



