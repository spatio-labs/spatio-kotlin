# InboxApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getInboxCounts**](InboxApi.md#getInboxCounts) | **GET** /v1/inbox/counts | Per-bucket unread counts. |
| [**listInbox**](InboxApi.md#listInbox) | **GET** /v1/inbox | Unified inbox feed across mail, channel mentions, DMs, system notifications. |
| [**markInboxItemRead**](InboxApi.md#markInboxItemRead) | **PATCH** /v1/inbox/{id}/read | Mark a single inbox item as read. |
| [**workspaceGetInboxCounts**](InboxApi.md#workspaceGetInboxCounts) | **GET** /v1/organizations/{org}/workspaces/{workspace}/inbox/counts |  |
| [**workspaceListInbox**](InboxApi.md#workspaceListInbox) | **GET** /v1/organizations/{org}/workspaces/{workspace}/inbox |  |
| [**workspaceMarkInboxItemRead**](InboxApi.md#workspaceMarkInboxItemRead) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/inbox/{id}/read |  |


<a id="getInboxCounts"></a>
# **getInboxCounts**
> InboxCounts getInboxCounts()

Per-bucket unread counts.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = InboxApi()
try {
    val result : InboxCounts = apiInstance.getInboxCounts()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling InboxApi#getInboxCounts")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling InboxApi#getInboxCounts")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InboxCounts**](InboxCounts.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listInbox"></a>
# **listInbox**
> InboxListResponse listInbox(category, unreadOnly, limit)

Unified inbox feed across mail, channel mentions, DMs, system notifications.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = InboxApi()
val category : kotlin.String = category_example // kotlin.String | 
val unreadOnly : kotlin.Boolean = true // kotlin.Boolean | 
val limit : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : InboxListResponse = apiInstance.listInbox(category, unreadOnly, limit)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling InboxApi#listInbox")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling InboxApi#listInbox")
    e.printStackTrace()
}
```

### Parameters
| **category** | **kotlin.String**|  | [optional] |
| **unreadOnly** | **kotlin.Boolean**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **kotlin.Int**|  | [optional] |

### Return type

[**InboxListResponse**](InboxListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="markInboxItemRead"></a>
# **markInboxItemRead**
> markInboxItemRead(id)

Mark a single inbox item as read.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = InboxApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.markInboxItemRead(id)
} catch (e: ClientException) {
    println("4xx response calling InboxApi#markInboxItemRead")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling InboxApi#markInboxItemRead")
    e.printStackTrace()
}
```

### Parameters
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

<a id="workspaceGetInboxCounts"></a>
# **workspaceGetInboxCounts**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetInboxCounts(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = InboxApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetInboxCounts(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling InboxApi#workspaceGetInboxCounts")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling InboxApi#workspaceGetInboxCounts")
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

<a id="workspaceListInbox"></a>
# **workspaceListInbox**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListInbox(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = InboxApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListInbox(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling InboxApi#workspaceListInbox")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling InboxApi#workspaceListInbox")
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

<a id="workspaceMarkInboxItemRead"></a>
# **workspaceMarkInboxItemRead**
> workspaceMarkInboxItemRead(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = InboxApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceMarkInboxItemRead(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling InboxApi#workspaceMarkInboxItemRead")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling InboxApi#workspaceMarkInboxItemRead")
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

