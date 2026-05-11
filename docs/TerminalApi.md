# TerminalApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTerminalSession**](TerminalApi.md#createTerminalSession) | **POST** /v1/terminal/sessions | Create a terminal session record. PTY bytes flow renderer ↔ local-agent over IPC and never traverse this API.  |
| [**deleteTerminalSession**](TerminalApi.md#deleteTerminalSession) | **DELETE** /v1/terminal/sessions/{id} | Delete a terminal session record. |
| [**getTerminalSession**](TerminalApi.md#getTerminalSession) | **GET** /v1/terminal/sessions/{id} | Fetch a terminal session. |
| [**listTerminalSessions**](TerminalApi.md#listTerminalSessions) | **GET** /v1/terminal/sessions | List the caller&#39;s terminal sessions (metadata only — no PTY bytes). |
| [**updateTerminalSession**](TerminalApi.md#updateTerminalSession) | **PATCH** /v1/terminal/sessions/{id} | Update terminal session metadata (title, cwd, etc.). |


<a id="createTerminalSession"></a>
# **createTerminalSession**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; createTerminalSession(requestBody)

Create a terminal session record. PTY bytes flow renderer ↔ local-agent over IPC and never traverse this API. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TerminalApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.createTerminalSession(requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TerminalApi#createTerminalSession")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TerminalApi#createTerminalSession")
    e.printStackTrace()
}
```

### Parameters
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

<a id="deleteTerminalSession"></a>
# **deleteTerminalSession**
> deleteTerminalSession(id)

Delete a terminal session record.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TerminalApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteTerminalSession(id)
} catch (e: ClientException) {
    println("4xx response calling TerminalApi#deleteTerminalSession")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TerminalApi#deleteTerminalSession")
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

<a id="getTerminalSession"></a>
# **getTerminalSession**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getTerminalSession(id)

Fetch a terminal session.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TerminalApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getTerminalSession(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TerminalApi#getTerminalSession")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TerminalApi#getTerminalSession")
    e.printStackTrace()
}
```

### Parameters
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

<a id="listTerminalSessions"></a>
# **listTerminalSessions**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listTerminalSessions()

List the caller&#39;s terminal sessions (metadata only — no PTY bytes).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TerminalApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listTerminalSessions()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TerminalApi#listTerminalSessions")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TerminalApi#listTerminalSessions")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateTerminalSession"></a>
# **updateTerminalSession**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateTerminalSession(id, requestBody)

Update terminal session metadata (title, cwd, etc.).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = TerminalApi()
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateTerminalSession(id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TerminalApi#updateTerminalSession")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TerminalApi#updateTerminalSession")
    e.printStackTrace()
}
```

### Parameters
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

