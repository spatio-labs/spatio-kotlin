# RealtimeApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**issueCollaborationToken**](RealtimeApi.md#issueCollaborationToken) | **POST** /v1/realtime/collaboration-token | Exchange a bearer token for a short-lived Yjs collaboration JWT. |


<a id="issueCollaborationToken"></a>
# **issueCollaborationToken**
> IssueCollaborationToken200Response issueCollaborationToken(issueCollaborationTokenRequest)

Exchange a bearer token for a short-lived Yjs collaboration JWT.

The Yjs Cloudflare Worker that powers live document collaboration (&#x60;wss://realtime-collaboration.&lt;account&gt;.workers.dev&#x60;) only accepts platform-signed JWTs. Third-party clients holding an OAuth access token or PAT call this endpoint to mint a 5-minute collaboration JWT they can present to the worker.  The minted JWT inherits user + workspace identity from the presenting bearer token. Optionally scope it to a single room by supplying &#x60;room&#x60; in the request body. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RealtimeApi()
val issueCollaborationTokenRequest : IssueCollaborationTokenRequest =  // IssueCollaborationTokenRequest | 
try {
    val result : IssueCollaborationToken200Response = apiInstance.issueCollaborationToken(issueCollaborationTokenRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RealtimeApi#issueCollaborationToken")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RealtimeApi#issueCollaborationToken")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **issueCollaborationTokenRequest** | [**IssueCollaborationTokenRequest**](IssueCollaborationTokenRequest.md)|  | [optional] |

### Return type

[**IssueCollaborationToken200Response**](IssueCollaborationToken200Response.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

