
# CreateTaskRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **title** | **kotlin.String** |  |  |
| **description** | **kotlin.String** |  |  [optional] |
| **status** | **kotlin.String** |  |  [optional] |
| **dueDate** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **priority** | [**inline**](#Priority) |  |  [optional] |
| **labels** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **tags** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **assigneeId** | **kotlin.String** |  |  [optional] |
| **parentTaskId** | **kotlin.String** |  |  [optional] |
| **type** | **kotlin.String** |  |  [optional] |
| **sourcePlatform** | **kotlin.String** |  |  [optional] |
| **sourceId** | **kotlin.String** |  |  [optional] |
| **accountId** | **kotlin.String** | Optional override for the target connected account. May also be passed as &#x60;?accountId&#x3D;&#x60;.  |  [optional] |
| **provider** | **kotlin.String** |  |  [optional] |


<a id="Priority"></a>
## Enum: priority
| Name | Value |
| ---- | ----- |
| priority | none, low, medium, high, urgent |



