# AppsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createApp**](AppsApi.md#createApp) | **POST** /v1/apps | Register a prototype app (project_path is the on-disk root). |
| [**deleteApp**](AppsApi.md#deleteApp) | **DELETE** /v1/apps/{id} | Delete an app. |
| [**deleteAppFile**](AppsApi.md#deleteAppFile) | **DELETE** /v1/apps/{id}/file | Delete one file inside the app&#39;s project directory. |
| [**getApp**](AppsApi.md#getApp) | **GET** /v1/apps/{id} | Fetch an app. |
| [**listAppFiles**](AppsApi.md#listAppFiles) | **GET** /v1/apps/{id}/files | List files inside the app&#39;s project directory. |
| [**listApps**](AppsApi.md#listApps) | **GET** /v1/apps | List the caller&#39;s prototype apps. |
| [**readAppFile**](AppsApi.md#readAppFile) | **GET** /v1/apps/{id}/file | Read one file inside the app&#39;s project directory. Path is traversal-checked; returns 400 if it escapes project root.  |
| [**updateApp**](AppsApi.md#updateApp) | **PATCH** /v1/apps/{id} | Update an app. |
| [**workspaceCreateApp**](AppsApi.md#workspaceCreateApp) | **POST** /v1/organizations/{org}/workspaces/{workspace}/apps |  |
| [**workspaceDeleteApp**](AppsApi.md#workspaceDeleteApp) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/apps/{id} |  |
| [**workspaceGetApp**](AppsApi.md#workspaceGetApp) | **GET** /v1/organizations/{org}/workspaces/{workspace}/apps/{id} |  |
| [**workspaceListApps**](AppsApi.md#workspaceListApps) | **GET** /v1/organizations/{org}/workspaces/{workspace}/apps |  |
| [**workspaceUpdateApp**](AppsApi.md#workspaceUpdateApp) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/apps/{id} |  |
| [**writeAppFile**](AppsApi.md#writeAppFile) | **POST** /v1/apps/{id}/file | Write one file inside the app&#39;s project directory. |


<a id="createApp"></a>
# **createApp**
> App createApp(createAppRequest)

Register a prototype app (project_path is the on-disk root).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val createAppRequest : CreateAppRequest =  // CreateAppRequest | 
try {
    val result : App = apiInstance.createApp(createAppRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#createApp")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#createApp")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createAppRequest** | [**CreateAppRequest**](CreateAppRequest.md)|  | |

### Return type

[**App**](App.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteApp"></a>
# **deleteApp**
> deleteApp(id)

Delete an app.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteApp(id)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#deleteApp")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#deleteApp")
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

<a id="deleteAppFile"></a>
# **deleteAppFile**
> deleteAppFile(id, path)

Delete one file inside the app&#39;s project directory.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val id : kotlin.String = id_example // kotlin.String | 
val path : kotlin.String = path_example // kotlin.String | 
try {
    apiInstance.deleteAppFile(id, path)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#deleteAppFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#deleteAppFile")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **path** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getApp"></a>
# **getApp**
> App getApp(id)

Fetch an app.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : App = apiInstance.getApp(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#getApp")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#getApp")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**App**](App.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listAppFiles"></a>
# **listAppFiles**
> AppFileListResponse listAppFiles(id, path)

List files inside the app&#39;s project directory.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val id : kotlin.String = id_example // kotlin.String | 
val path : kotlin.String = path_example // kotlin.String | 
try {
    val result : AppFileListResponse = apiInstance.listAppFiles(id, path)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#listAppFiles")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#listAppFiles")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **path** | **kotlin.String**|  | [optional] |

### Return type

[**AppFileListResponse**](AppFileListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listApps"></a>
# **listApps**
> AppListResponse listApps()

List the caller&#39;s prototype apps.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
try {
    val result : AppListResponse = apiInstance.listApps()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#listApps")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#listApps")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AppListResponse**](AppListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="readAppFile"></a>
# **readAppFile**
> AppFileContentResponse readAppFile(id, path)

Read one file inside the app&#39;s project directory. Path is traversal-checked; returns 400 if it escapes project root. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val id : kotlin.String = id_example // kotlin.String | 
val path : kotlin.String = path_example // kotlin.String | 
try {
    val result : AppFileContentResponse = apiInstance.readAppFile(id, path)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#readAppFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#readAppFile")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **path** | **kotlin.String**|  | |

### Return type

[**AppFileContentResponse**](AppFileContentResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateApp"></a>
# **updateApp**
> App updateApp(id, updateAppRequest)

Update an app.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateAppRequest : UpdateAppRequest =  // UpdateAppRequest | 
try {
    val result : App = apiInstance.updateApp(id, updateAppRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#updateApp")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#updateApp")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateAppRequest** | [**UpdateAppRequest**](UpdateAppRequest.md)|  | |

### Return type

[**App**](App.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceCreateApp"></a>
# **workspaceCreateApp**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateApp(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateApp(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#workspaceCreateApp")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#workspaceCreateApp")
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

<a id="workspaceDeleteApp"></a>
# **workspaceDeleteApp**
> workspaceDeleteApp(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceDeleteApp(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#workspaceDeleteApp")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#workspaceDeleteApp")
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

<a id="workspaceGetApp"></a>
# **workspaceGetApp**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetApp(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetApp(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#workspaceGetApp")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#workspaceGetApp")
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

<a id="workspaceListApps"></a>
# **workspaceListApps**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListApps(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListApps(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#workspaceListApps")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#workspaceListApps")
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

<a id="workspaceUpdateApp"></a>
# **workspaceUpdateApp**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUpdateApp(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUpdateApp(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#workspaceUpdateApp")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#workspaceUpdateApp")
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

<a id="writeAppFile"></a>
# **writeAppFile**
> writeAppFile(id, writeAppFileRequest)

Write one file inside the app&#39;s project directory.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AppsApi()
val id : kotlin.String = id_example // kotlin.String | 
val writeAppFileRequest : WriteAppFileRequest =  // WriteAppFileRequest | 
try {
    apiInstance.writeAppFile(id, writeAppFileRequest)
} catch (e: ClientException) {
    println("4xx response calling AppsApi#writeAppFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AppsApi#writeAppFile")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **writeAppFileRequest** | [**WriteAppFileRequest**](WriteAppFileRequest.md)|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

