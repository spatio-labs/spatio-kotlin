# ModelsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createModel**](ModelsApi.md#createModel) | **POST** /v1/models | Register a model (admin-only). |
| [**deleteModel**](ModelsApi.md#deleteModel) | **DELETE** /v1/models/{id} | Delete a model (admin-only). |
| [**getActiveModel**](ModelsApi.md#getActiveModel) | **GET** /v1/models/active | Get the active model for a given provider. |
| [**getModel**](ModelsApi.md#getModel) | **GET** /v1/models/{id} | Fetch a model. |
| [**listModels**](ModelsApi.md#listModels) | **GET** /v1/models | List every LLM model the platform knows about. |
| [**setActiveModel**](ModelsApi.md#setActiveModel) | **POST** /v1/models/{id}/activate | Set a model as the active default for its provider (admin-only). |
| [**updateModel**](ModelsApi.md#updateModel) | **PATCH** /v1/models/{id} | Update a model (admin-only). |


<a id="createModel"></a>
# **createModel**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; createModel(requestBody)

Register a model (admin-only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ModelsApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.createModel(requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ModelsApi#createModel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ModelsApi#createModel")
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

<a id="deleteModel"></a>
# **deleteModel**
> deleteModel(id)

Delete a model (admin-only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ModelsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteModel(id)
} catch (e: ClientException) {
    println("4xx response calling ModelsApi#deleteModel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ModelsApi#deleteModel")
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

<a id="getActiveModel"></a>
# **getActiveModel**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getActiveModel(provider)

Get the active model for a given provider.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ModelsApi()
val provider : kotlin.String = provider_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getActiveModel(provider)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ModelsApi#getActiveModel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ModelsApi#getActiveModel")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **provider** | **kotlin.String**|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getModel"></a>
# **getModel**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getModel(id)

Fetch a model.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ModelsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getModel(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ModelsApi#getModel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ModelsApi#getModel")
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

<a id="listModels"></a>
# **listModels**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listModels()

List every LLM model the platform knows about.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ModelsApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listModels()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ModelsApi#listModels")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ModelsApi#listModels")
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

<a id="setActiveModel"></a>
# **setActiveModel**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; setActiveModel(id)

Set a model as the active default for its provider (admin-only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ModelsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.setActiveModel(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ModelsApi#setActiveModel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ModelsApi#setActiveModel")
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

<a id="updateModel"></a>
# **updateModel**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateModel(id, requestBody)

Update a model (admin-only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ModelsApi()
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateModel(id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ModelsApi#updateModel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ModelsApi#updateModel")
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

