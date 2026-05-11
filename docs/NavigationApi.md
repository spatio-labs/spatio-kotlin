# NavigationApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getNavigation**](NavigationApi.md#getNavigation) | **GET** /v1/navigation | Sidebar/navigation tree for the renderer. |


<a id="getNavigation"></a>
# **getNavigation**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getNavigation()

Sidebar/navigation tree for the renderer.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NavigationApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getNavigation()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NavigationApi#getNavigation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NavigationApi#getNavigation")
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

