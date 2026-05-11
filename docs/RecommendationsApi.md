# RecommendationsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteRecommendation**](RecommendationsApi.md#deleteRecommendation) | **DELETE** /v1/recommendations/{id} | Delete a recommendation (hard delete; status-update is preferred). |
| [**getRecommendation**](RecommendationsApi.md#getRecommendation) | **GET** /v1/recommendations/{id} | Fetch one recommendation. |
| [**listRecommendations**](RecommendationsApi.md#listRecommendations) | **GET** /v1/recommendations | List recommendations for a workspace. |
| [**proposeRecommendation**](RecommendationsApi.md#proposeRecommendation) | **POST** /v1/recommendations | Agent-side propose endpoint (the &#x60;spatio_recommendations propose&#x60; MCP tool calls this). |
| [**updateRecommendationStatus**](RecommendationsApi.md#updateRecommendationStatus) | **PATCH** /v1/recommendations/{id}/status | Accept or dismiss a recommendation. |


<a id="deleteRecommendation"></a>
# **deleteRecommendation**
> deleteRecommendation(id)

Delete a recommendation (hard delete; status-update is preferred).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecommendationsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteRecommendation(id)
} catch (e: ClientException) {
    println("4xx response calling RecommendationsApi#deleteRecommendation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecommendationsApi#deleteRecommendation")
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

<a id="getRecommendation"></a>
# **getRecommendation**
> Recommendation getRecommendation(id)

Fetch one recommendation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecommendationsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : Recommendation = apiInstance.getRecommendation(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RecommendationsApi#getRecommendation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecommendationsApi#getRecommendation")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**Recommendation**](Recommendation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listRecommendations"></a>
# **listRecommendations**
> RecommendationListResponse listRecommendations(workspaceId, status, limit)

List recommendations for a workspace.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecommendationsApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val status : kotlin.String = status_example // kotlin.String | 
val limit : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : RecommendationListResponse = apiInstance.listRecommendations(workspaceId, status, limit)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RecommendationsApi#listRecommendations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecommendationsApi#listRecommendations")
    e.printStackTrace()
}
```

### Parameters
| **workspaceId** | **kotlin.String**|  | [optional] |
| **status** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **kotlin.Int**|  | [optional] |

### Return type

[**RecommendationListResponse**](RecommendationListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="proposeRecommendation"></a>
# **proposeRecommendation**
> Recommendation proposeRecommendation(proposeRecommendationRequest)

Agent-side propose endpoint (the &#x60;spatio_recommendations propose&#x60; MCP tool calls this).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecommendationsApi()
val proposeRecommendationRequest : ProposeRecommendationRequest =  // ProposeRecommendationRequest | 
try {
    val result : Recommendation = apiInstance.proposeRecommendation(proposeRecommendationRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RecommendationsApi#proposeRecommendation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecommendationsApi#proposeRecommendation")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **proposeRecommendationRequest** | [**ProposeRecommendationRequest**](ProposeRecommendationRequest.md)|  | |

### Return type

[**Recommendation**](Recommendation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateRecommendationStatus"></a>
# **updateRecommendationStatus**
> Recommendation updateRecommendationStatus(id, updateRecommendationStatusRequest)

Accept or dismiss a recommendation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecommendationsApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateRecommendationStatusRequest : UpdateRecommendationStatusRequest =  // UpdateRecommendationStatusRequest | 
try {
    val result : Recommendation = apiInstance.updateRecommendationStatus(id, updateRecommendationStatusRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RecommendationsApi#updateRecommendationStatus")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecommendationsApi#updateRecommendationStatus")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateRecommendationStatusRequest** | [**UpdateRecommendationStatusRequest**](UpdateRecommendationStatusRequest.md)|  | |

### Return type

[**Recommendation**](Recommendation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

