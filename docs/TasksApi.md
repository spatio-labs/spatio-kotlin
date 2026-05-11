# TasksApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**bulkDeleteTasks**](TasksApi.md#bulkDeleteTasks) | **POST** /v1/tasks/delete | Delete multiple tasks in one call. |
| [**bulkUpdateTasks**](TasksApi.md#bulkUpdateTasks) | **POST** /v1/tasks/bulk-update | Apply the same update to multiple tasks. |
| [**completeTask**](TasksApi.md#completeTask) | **POST** /v1/tasks/{id}/complete | Mark a task complete. |
| [**createTask**](TasksApi.md#createTask) | **POST** /v1/tasks | Create a task. |
| [**createTaskComment**](TasksApi.md#createTaskComment) | **POST** /v1/tasks/{id}/comments | Create a comment. |
| [**deleteTask**](TasksApi.md#deleteTask) | **DELETE** /v1/tasks/{id} | Delete a task. |
| [**deleteTaskComment**](TasksApi.md#deleteTaskComment) | **DELETE** /v1/tasks/{id}/comments/{commentId} | Delete a task comment. |
| [**getTask**](TasksApi.md#getTask) | **GET** /v1/tasks/{id} | Fetch one task. |
| [**listTaskComments**](TasksApi.md#listTaskComments) | **GET** /v1/tasks/{id}/comments | List comments on a task. |
| [**listTaskProviders**](TasksApi.md#listTaskProviders) | **GET** /v1/tasks/providers | List supported task providers. |
| [**listTasks**](TasksApi.md#listTasks) | **GET** /v1/tasks | List tasks across connected accounts. |
| [**updateTask**](TasksApi.md#updateTask) | **PATCH** /v1/tasks/{id} | Update a task (partial). |
| [**updateTaskComment**](TasksApi.md#updateTaskComment) | **PATCH** /v1/tasks/{id}/comments/{commentId} | Edit a task comment. |
| [**workspaceCompleteTask**](TasksApi.md#workspaceCompleteTask) | **POST** /v1/organizations/{org}/workspaces/{workspace}/tasks/{id}/complete |  |
| [**workspaceCompleteTaskAlias**](TasksApi.md#workspaceCompleteTaskAlias) | **POST** /v1/organizations/{org}/workspaces/{workspace}/tasks/complete/task | Renderer-compat alias for /tasks/{id}/complete. |
| [**workspaceCreateTask**](TasksApi.md#workspaceCreateTask) | **POST** /v1/organizations/{org}/workspaces/{workspace}/tasks |  |
| [**workspaceCreateTaskAlias**](TasksApi.md#workspaceCreateTaskAlias) | **POST** /v1/organizations/{org}/workspaces/{workspace}/tasks/task | Renderer-compat alias for POST /tasks. |
| [**workspaceDeleteTask**](TasksApi.md#workspaceDeleteTask) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/tasks/{id} |  |
| [**workspaceGetTask**](TasksApi.md#workspaceGetTask) | **GET** /v1/organizations/{org}/workspaces/{workspace}/tasks/{id} |  |
| [**workspaceListTaskProviders**](TasksApi.md#workspaceListTaskProviders) | **GET** /v1/organizations/{org}/workspaces/{workspace}/tasks/providers |  |
| [**workspaceListTasks**](TasksApi.md#workspaceListTasks) | **GET** /v1/organizations/{org}/workspaces/{workspace}/tasks |  |
| [**workspaceListTasksAlias**](TasksApi.md#workspaceListTasksAlias) | **GET** /v1/organizations/{org}/workspaces/{workspace}/tasks/tasks | Renderer-compat alias for /tasks. |
| [**workspaceUpdateTask**](TasksApi.md#workspaceUpdateTask) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/tasks/{id} |  |
| [**workspaceUpdateTaskAlias**](TasksApi.md#workspaceUpdateTaskAlias) | **PUT** /v1/organizations/{org}/workspaces/{workspace}/tasks/task/{id} | Renderer-compat alias for PATCH /tasks/{id}. |


<a id="bulkDeleteTasks"></a>
# **bulkDeleteTasks**
> BulkDeleteTasksResponse bulkDeleteTasks(bulkDeleteTasksRequest)

Delete multiple tasks in one call.

Replaces the legacy BFF that looped DELETE /v1/tasks/:id. Per-id errors are collected in &#x60;failed&#x60; rather than failing the whole call — partial success is the norm. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val bulkDeleteTasksRequest : BulkDeleteTasksRequest =  // BulkDeleteTasksRequest | 
try {
    val result : BulkDeleteTasksResponse = apiInstance.bulkDeleteTasks(bulkDeleteTasksRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#bulkDeleteTasks")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#bulkDeleteTasks")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bulkDeleteTasksRequest** | [**BulkDeleteTasksRequest**](BulkDeleteTasksRequest.md)|  | |

### Return type

[**BulkDeleteTasksResponse**](BulkDeleteTasksResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="bulkUpdateTasks"></a>
# **bulkUpdateTasks**
> BulkUpdateTasksResponse bulkUpdateTasks(bulkUpdateTasksRequest)

Apply the same update to multiple tasks.

Same &#x60;updates&#x60; payload applied to every id in &#x60;taskIds&#x60;. As with bulk delete, per-id failures collect in &#x60;failed&#x60;. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val bulkUpdateTasksRequest : BulkUpdateTasksRequest =  // BulkUpdateTasksRequest | 
try {
    val result : BulkUpdateTasksResponse = apiInstance.bulkUpdateTasks(bulkUpdateTasksRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#bulkUpdateTasks")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#bulkUpdateTasks")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bulkUpdateTasksRequest** | [**BulkUpdateTasksRequest**](BulkUpdateTasksRequest.md)|  | |

### Return type

[**BulkUpdateTasksResponse**](BulkUpdateTasksResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="completeTask"></a>
# **completeTask**
> SuccessFlag completeTask(id, accountId, xWorkspaceID)

Mark a task complete.

Idempotent — completing an already-completed task is a no-op that still returns success. The legacy &#x60;POST /v1/tasks/complete/task&#x60; endpoint accepts the same operation with the task id in the JSON body instead of the URL; that variant is a renderer-compat shim and is not modeled in the spec. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val id : kotlin.String = id_example // kotlin.String | Task id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.completeTask(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#completeTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#completeTask")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Task id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="createTask"></a>
# **createTask**
> Task createTask(createTaskRequest, accountId, provider, xWorkspaceID)

Create a task.

Creates a new task under the target account. Target resolution mirrors &#x60;POST /v1/notes&#x60;: body &#x60;accountId&#x60; → &#x60;?accountId&#x3D;&#x60; → body &#x60;provider&#x60; → &#x60;?provider&#x3D;&#x60; → caller&#39;s single connected account (errors &#x60;ambiguous_account&#x60; if more than one and no selector). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val createTaskRequest : CreateTaskRequest =  // CreateTaskRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Task = apiInstance.createTask(createTaskRequest, accountId, provider, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#createTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#createTask")
    e.printStackTrace()
}
```

### Parameters
| **createTaskRequest** | [**CreateTaskRequest**](CreateTaskRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **provider** | **kotlin.String**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Task**](Task.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createTaskComment"></a>
# **createTaskComment**
> TaskCommentMutationResponse createTaskComment(id, taskCommentRequest, accountId, xWorkspaceID)

Create a comment.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val id : kotlin.String = id_example // kotlin.String | Task id.
val taskCommentRequest : TaskCommentRequest =  // TaskCommentRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : TaskCommentMutationResponse = apiInstance.createTaskComment(id, taskCommentRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#createTaskComment")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#createTaskComment")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Task id. | |
| **taskCommentRequest** | [**TaskCommentRequest**](TaskCommentRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**TaskCommentMutationResponse**](TaskCommentMutationResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteTask"></a>
# **deleteTask**
> SuccessFlag deleteTask(id, accountId, xWorkspaceID)

Delete a task.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val id : kotlin.String = id_example // kotlin.String | Task id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.deleteTask(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#deleteTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#deleteTask")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Task id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="deleteTaskComment"></a>
# **deleteTaskComment**
> SuccessFlag deleteTaskComment(id, commentId, accountId, xWorkspaceID)

Delete a task comment.

Allowed for the comment author and (for native comments) for the task owner. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val id : kotlin.String = id_example // kotlin.String | Task id.
val commentId : kotlin.String = commentId_example // kotlin.String | Comment id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.deleteTaskComment(id, commentId, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#deleteTaskComment")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#deleteTaskComment")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Task id. | |
| **commentId** | **kotlin.String**| Comment id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getTask"></a>
# **getTask**
> Task getTask(id, accountId, xWorkspaceID)

Fetch one task.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val id : kotlin.String = id_example // kotlin.String | Task id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Task = apiInstance.getTask(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#getTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#getTask")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Task id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Task**](Task.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listTaskComments"></a>
# **listTaskComments**
> TaskCommentList listTaskComments(id, accountId, xWorkspaceID)

List comments on a task.

Returns active comments. When &#x60;?accountId&#x3D;&#x60; targets an external provider that supports comments (e.g. Linear), the provider is queried directly; otherwise the native &#x60;TaskComment&#x60; table is used. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val id : kotlin.String = id_example // kotlin.String | Task id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : TaskCommentList = apiInstance.listTaskComments(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#listTaskComments")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#listTaskComments")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Task id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**TaskCommentList**](TaskCommentList.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listTaskProviders"></a>
# **listTaskProviders**
> TaskProvidersInfo listTaskProviders()

List supported task providers.

Returns the registered task-provider ids and the platform&#39;s own metadata. Useful for clients that need to render provider-specific UI (icons, capability flags) before committing to a particular &#x60;provider&#x60;. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
try {
    val result : TaskProvidersInfo = apiInstance.listTaskProviders()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#listTaskProviders")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#listTaskProviders")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**TaskProvidersInfo**](TaskProvidersInfo.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listTasks"></a>
# **listTasks**
> TaskListEnvelope listTasks(accountId, provider, xWorkspaceID, completed, labels, parentTaskId, type, sourcePlatform, sourceId, limit, offset)

List tasks across connected accounts.

Fan-out list. Returns every task visible to the caller across every connected tasks provider. Pass &#x60;?accountId&#x3D;&#x60; or &#x60;?provider&#x3D;&#x60; to scope to a single source. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val completed : kotlin.Boolean = true // kotlin.Boolean | Include completed tasks. Default `false` (active tasks only). 
val labels : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Filter to tasks carrying every label listed.
val parentTaskId : kotlin.String = parentTaskId_example // kotlin.String | Filter to subtasks of this parent.
val type : kotlin.String = type_example // kotlin.String | Discriminator filter (`todo`, `reminder`, `issue`). 
val sourcePlatform : kotlin.String = sourcePlatform_example // kotlin.String | Filter to tasks linked to a given source platform.
val sourceId : kotlin.String = sourceId_example // kotlin.String | Filter to tasks linked to a specific source artifact id. Pair with `sourcePlatform` for an exact match. 
val limit : kotlin.Int = 56 // kotlin.Int | 
val offset : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : TaskListEnvelope = apiInstance.listTasks(accountId, provider, xWorkspaceID, completed, labels, parentTaskId, type, sourcePlatform, sourceId, limit, offset)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#listTasks")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#listTasks")
    e.printStackTrace()
}
```

### Parameters
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **provider** | **kotlin.String**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **completed** | **kotlin.Boolean**| Include completed tasks. Default &#x60;false&#x60; (active tasks only).  | [optional] [default to false] |
| **labels** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Filter to tasks carrying every label listed. | [optional] |
| **parentTaskId** | **kotlin.String**| Filter to subtasks of this parent. | [optional] |
| **type** | **kotlin.String**| Discriminator filter (&#x60;todo&#x60;, &#x60;reminder&#x60;, &#x60;issue&#x60;).  | [optional] |
| **sourcePlatform** | **kotlin.String**| Filter to tasks linked to a given source platform. | [optional] |
| **sourceId** | **kotlin.String**| Filter to tasks linked to a specific source artifact id. Pair with &#x60;sourcePlatform&#x60; for an exact match.  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] [default to 50] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **kotlin.Int**|  | [optional] [default to 0] |

### Return type

[**TaskListEnvelope**](TaskListEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateTask"></a>
# **updateTask**
> Task updateTask(id, updateTaskRequest, accountId, xWorkspaceID)

Update a task (partial).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val id : kotlin.String = id_example // kotlin.String | Task id.
val updateTaskRequest : UpdateTaskRequest =  // UpdateTaskRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Task = apiInstance.updateTask(id, updateTaskRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#updateTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#updateTask")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Task id. | |
| **updateTaskRequest** | [**UpdateTaskRequest**](UpdateTaskRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Task**](Task.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateTaskComment"></a>
# **updateTaskComment**
> TaskCommentMutationResponse updateTaskComment(id, commentId, taskCommentRequest, accountId, xWorkspaceID)

Edit a task comment.

Only the comment author can edit.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val id : kotlin.String = id_example // kotlin.String | Task id.
val commentId : kotlin.String = commentId_example // kotlin.String | Comment id.
val taskCommentRequest : TaskCommentRequest =  // TaskCommentRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : TaskCommentMutationResponse = apiInstance.updateTaskComment(id, commentId, taskCommentRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#updateTaskComment")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#updateTaskComment")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Task id. | |
| **commentId** | **kotlin.String**| Comment id. | |
| **taskCommentRequest** | [**TaskCommentRequest**](TaskCommentRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**TaskCommentMutationResponse**](TaskCommentMutationResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceCompleteTask"></a>
# **workspaceCompleteTask**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCompleteTask(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCompleteTask(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#workspaceCompleteTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#workspaceCompleteTask")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceCompleteTaskAlias"></a>
# **workspaceCompleteTaskAlias**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCompleteTaskAlias(org, workspace, requestBody)

Renderer-compat alias for /tasks/{id}/complete.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCompleteTaskAlias(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#workspaceCompleteTaskAlias")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#workspaceCompleteTaskAlias")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **requestBody** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceCreateTask"></a>
# **workspaceCreateTask**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateTask(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateTask(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#workspaceCreateTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#workspaceCreateTask")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **requestBody** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceCreateTaskAlias"></a>
# **workspaceCreateTaskAlias**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateTaskAlias(org, workspace, requestBody)

Renderer-compat alias for POST /tasks.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateTaskAlias(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#workspaceCreateTaskAlias")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#workspaceCreateTaskAlias")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **requestBody** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceDeleteTask"></a>
# **workspaceDeleteTask**
> workspaceDeleteTask(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceDeleteTask(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#workspaceDeleteTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#workspaceDeleteTask")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceGetTask"></a>
# **workspaceGetTask**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetTask(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetTask(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#workspaceGetTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#workspaceGetTask")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceListTaskProviders"></a>
# **workspaceListTaskProviders**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListTaskProviders(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListTaskProviders(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#workspaceListTaskProviders")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#workspaceListTaskProviders")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceListTasks"></a>
# **workspaceListTasks**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListTasks(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListTasks(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#workspaceListTasks")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#workspaceListTasks")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceListTasksAlias"></a>
# **workspaceListTasksAlias**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListTasksAlias(org, workspace)

Renderer-compat alias for /tasks.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListTasksAlias(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#workspaceListTasksAlias")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#workspaceListTasksAlias")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceUpdateTask"></a>
# **workspaceUpdateTask**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUpdateTask(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUpdateTask(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#workspaceUpdateTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#workspaceUpdateTask")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **requestBody** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceUpdateTaskAlias"></a>
# **workspaceUpdateTaskAlias**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUpdateTaskAlias(org, workspace, id, requestBody)

Renderer-compat alias for PATCH /tasks/{id}.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TasksApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUpdateTaskAlias(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TasksApi#workspaceUpdateTaskAlias")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TasksApi#workspaceUpdateTaskAlias")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **requestBody** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

