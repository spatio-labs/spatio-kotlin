# SearchApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**federatedSearch**](SearchApi.md#federatedSearch) | **POST** /v1/search | Cross-platform federated search. |


<a id="federatedSearch"></a>
# **federatedSearch**
> FederatedSearch200Response federatedSearch(federatedSearchRequest)

Cross-platform federated search.

Fans out to every platform&#39;s per-platform search method in parallel, merges + dedupes results, and returns them in a relevance-then-recency ranking with per-platform cursors for pagination. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SearchApi()
val federatedSearchRequest : FederatedSearchRequest =  // FederatedSearchRequest | 
try {
    val result : FederatedSearch200Response = apiInstance.federatedSearch(federatedSearchRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SearchApi#federatedSearch")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SearchApi#federatedSearch")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **federatedSearchRequest** | [**FederatedSearchRequest**](FederatedSearchRequest.md)|  | |

### Return type

[**FederatedSearch200Response**](FederatedSearch200Response.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

