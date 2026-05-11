
# Task

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** |  |  |
| **title** | **kotlin.String** |  |  |
| **completed** | **kotlin.Boolean** |  |  |
| **priority** | [**inline**](#Priority) | Priority bucket. Canonical values (mapped from a 0–4 integer): &#x60;none&#x60;, &#x60;low&#x60;, &#x60;medium&#x60;, &#x60;high&#x60;, &#x60;urgent&#x60;.  |  |
| **createdAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **updatedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **provider** | **kotlin.String** | Registered provider id (e.g. &#x60;native-tasks&#x60;, &#x60;linear&#x60;). |  [optional] |
| **accountId** | **kotlin.String** |  |  [optional] |
| **ownerUserId** | **kotlin.String** |  |  [optional] |
| **description** | **kotlin.String** |  |  [optional] |
| **status** | **kotlin.String** | Free-form status string. Canonical values across most providers: &#x60;todo&#x60;, &#x60;in_progress&#x60;, &#x60;in_review&#x60;, &#x60;backlog&#x60;, &#x60;done&#x60;. The platform falls back to &#x60;done&#x60; when &#x60;completed&#x60; is true and &#x60;status&#x60; is empty, else &#x60;todo&#x60;.  |  [optional] |
| **dueDate** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **labels** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **tags** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **assigneeId** | **kotlin.String** |  |  [optional] |
| **completedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **parentTaskId** | **kotlin.String** | Parent task id when this is a subtask. |  [optional] |
| **metadata** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md) | Provider-specific extras. |  [optional] |
| **type** | **kotlin.String** | Discriminator. Canonical values: &#x60;todo&#x60;, &#x60;reminder&#x60;, &#x60;issue&#x60;. Empty defaults to &#x60;todo&#x60;.  |  [optional] |
| **sourcePlatform** | **kotlin.String** | When this task was auto-generated from another artifact (e.g. a calendar event reminder), the platform id of that artifact.  |  [optional] |
| **sourceId** | **kotlin.String** | Source artifact id paired with &#x60;sourcePlatform&#x60;. |  [optional] |


<a id="Priority"></a>
## Enum: priority
| Name | Value |
| ---- | ----- |
| priority | none, low, medium, high, urgent |



