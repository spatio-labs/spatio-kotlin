# ResourcesApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listResourcePermissionGrants**](ResourcesApi.md#listResourcePermissionGrants) | **GET** /v1/resources/{platform}/{resourceId}/permissions | List access grants on a resource (per-resource ACL). |
| [**revokeResourcePermissionGrant**](ResourcesApi.md#revokeResourcePermissionGrant) | **DELETE** /v1/resources/{platform}/{resourceId}/permissions/{grantId} | Revoke an access grant. |
| [**setResourcePermissionGrant**](ResourcesApi.md#setResourcePermissionGrant) | **POST** /v1/resources/{platform}/{resourceId}/permissions | Create or update an access grant. |


<a id="listResourcePermissionGrants"></a>
# **listResourcePermissionGrants**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listResourcePermissionGrants(platform, resourceId)

List access grants on a resource (per-resource ACL).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ResourcesApi()
val platform : kotlin.String = platform_example // kotlin.String | 
val resourceId : kotlin.String = resourceId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listResourcePermissionGrants(platform, resourceId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ResourcesApi#listResourcePermissionGrants")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ResourcesApi#listResourcePermissionGrants")
    e.printStackTrace()
}
```

### Parameters
| **platform** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **resourceId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="revokeResourcePermissionGrant"></a>
# **revokeResourcePermissionGrant**
> revokeResourcePermissionGrant(platform, resourceId, grantId)

Revoke an access grant.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ResourcesApi()
val platform : kotlin.String = platform_example // kotlin.String | 
val resourceId : kotlin.String = resourceId_example // kotlin.String | 
val grantId : kotlin.String = grantId_example // kotlin.String | 
try {
    apiInstance.revokeResourcePermissionGrant(platform, resourceId, grantId)
} catch (e: ClientException) {
    println("4xx response calling ResourcesApi#revokeResourcePermissionGrant")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ResourcesApi#revokeResourcePermissionGrant")
    e.printStackTrace()
}
```

### Parameters
| **platform** | **kotlin.String**|  | |
| **resourceId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **grantId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="setResourcePermissionGrant"></a>
# **setResourcePermissionGrant**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; setResourcePermissionGrant(platform, resourceId, requestBody)

Create or update an access grant.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ResourcesApi()
val platform : kotlin.String = platform_example // kotlin.String | 
val resourceId : kotlin.String = resourceId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.setResourcePermissionGrant(platform, resourceId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ResourcesApi#setResourcePermissionGrant")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ResourcesApi#setResourcePermissionGrant")
    e.printStackTrace()
}
```

### Parameters
| **platform** | **kotlin.String**|  | |
| **resourceId** | **kotlin.String**|  | |
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

