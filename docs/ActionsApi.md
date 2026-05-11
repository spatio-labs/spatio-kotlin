# ActionsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**executeAction**](ActionsApi.md#executeAction) | **POST** /v1/actions/execute | Renderer-side execute alias. The canonical endpoint is &#x60;POST /v1/agent/actions/execute&#x60;; this path delegates to the same handler.  |
| [**getCoreAction**](ActionsApi.md#getCoreAction) | **GET** /v1/actions/core/{id} | Fetch a single core action by id. |
| [**listAvailableActions**](ActionsApi.md#listAvailableActions) | **GET** /v1/actions/available | List every action the agent platform exposes. |
| [**listCoreActions**](ActionsApi.md#listCoreActions) | **GET** /v1/actions/core | List renderer-curated \&quot;core actions\&quot; (command-palette + keybindings backing). |
| [**listCoreActionsByPlatform**](ActionsApi.md#listCoreActionsByPlatform) | **GET** /v1/actions/core/platform/{platform} | Core actions filtered to one platform. |
| [**listPlatformActions**](ActionsApi.md#listPlatformActions) | **GET** /v1/actions/platform/{platform} | List actions tagged for a specific platform (notes, mail, ...). |


<a id="executeAction"></a>
# **executeAction**
> ExecuteActionResponse executeAction(executeActionRequest)

Renderer-side execute alias. The canonical endpoint is &#x60;POST /v1/agent/actions/execute&#x60;; this path delegates to the same handler. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ActionsApi()
val executeActionRequest : ExecuteActionRequest =  // ExecuteActionRequest | 
try {
    val result : ExecuteActionResponse = apiInstance.executeAction(executeActionRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ActionsApi#executeAction")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ActionsApi#executeAction")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **executeActionRequest** | [**ExecuteActionRequest**](ExecuteActionRequest.md)|  | |

### Return type

[**ExecuteActionResponse**](ExecuteActionResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="getCoreAction"></a>
# **getCoreAction**
> CoreAction getCoreAction(id)

Fetch a single core action by id.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ActionsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : CoreAction = apiInstance.getCoreAction(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ActionsApi#getCoreAction")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ActionsApi#getCoreAction")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**CoreAction**](CoreAction.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listAvailableActions"></a>
# **listAvailableActions**
> kotlin.collections.List&lt;ActionDescriptor&gt; listAvailableActions()

List every action the agent platform exposes.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ActionsApi()
try {
    val result : kotlin.collections.List<ActionDescriptor> = apiInstance.listAvailableActions()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ActionsApi#listAvailableActions")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ActionsApi#listAvailableActions")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**kotlin.collections.List&lt;ActionDescriptor&gt;**](ActionDescriptor.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listCoreActions"></a>
# **listCoreActions**
> CoreActionListResponse listCoreActions()

List renderer-curated \&quot;core actions\&quot; (command-palette + keybindings backing).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ActionsApi()
try {
    val result : CoreActionListResponse = apiInstance.listCoreActions()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ActionsApi#listCoreActions")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ActionsApi#listCoreActions")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**CoreActionListResponse**](CoreActionListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listCoreActionsByPlatform"></a>
# **listCoreActionsByPlatform**
> CoreActionListResponse listCoreActionsByPlatform(platform)

Core actions filtered to one platform.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ActionsApi()
val platform : kotlin.String = platform_example // kotlin.String | 
try {
    val result : CoreActionListResponse = apiInstance.listCoreActionsByPlatform(platform)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ActionsApi#listCoreActionsByPlatform")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ActionsApi#listCoreActionsByPlatform")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platform** | **kotlin.String**|  | |

### Return type

[**CoreActionListResponse**](CoreActionListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listPlatformActions"></a>
# **listPlatformActions**
> kotlin.collections.List&lt;ActionDescriptor&gt; listPlatformActions(platform)

List actions tagged for a specific platform (notes, mail, ...).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ActionsApi()
val platform : kotlin.String = platform_example // kotlin.String | 
try {
    val result : kotlin.collections.List<ActionDescriptor> = apiInstance.listPlatformActions(platform)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ActionsApi#listPlatformActions")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ActionsApi#listPlatformActions")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platform** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.List&lt;ActionDescriptor&gt;**](ActionDescriptor.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

