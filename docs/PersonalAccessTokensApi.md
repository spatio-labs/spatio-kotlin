# PersonalAccessTokensApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createPersonalAccessToken**](PersonalAccessTokensApi.md#createPersonalAccessToken) | **POST** /v1/tokens | Create a new PAT. The full token is returned only once on creation; the API never reveals the secret again.  |
| [**listAvailablePATScopes**](PersonalAccessTokensApi.md#listAvailablePATScopes) | **GET** /v1/tokens/scopes | List the scope strings PATs can be issued with. |
| [**listPersonalAccessTokens**](PersonalAccessTokensApi.md#listPersonalAccessTokens) | **GET** /v1/tokens | List the caller&#39;s personal access tokens (with available scopes). |
| [**revokePersonalAccessToken**](PersonalAccessTokensApi.md#revokePersonalAccessToken) | **DELETE** /v1/tokens/{id} | Revoke a PAT. |
| [**updatePersonalAccessToken**](PersonalAccessTokensApi.md#updatePersonalAccessToken) | **PATCH** /v1/tokens/{id} | Rename or re-describe a PAT (scopes are immutable). |
| [**workspaceCreatePAT**](PersonalAccessTokensApi.md#workspaceCreatePAT) | **POST** /v1/organizations/{org}/workspaces/{workspace}/tokens |  |
| [**workspaceListPATs**](PersonalAccessTokensApi.md#workspaceListPATs) | **GET** /v1/organizations/{org}/workspaces/{workspace}/tokens |  |
| [**workspaceRevokePAT**](PersonalAccessTokensApi.md#workspaceRevokePAT) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/tokens/{id} |  |
| [**workspaceUpdatePAT**](PersonalAccessTokensApi.md#workspaceUpdatePAT) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/tokens/{id} |  |


<a id="createPersonalAccessToken"></a>
# **createPersonalAccessToken**
> CreatePATResponse createPersonalAccessToken(createPATRequest)

Create a new PAT. The full token is returned only once on creation; the API never reveals the secret again. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PersonalAccessTokensApi()
val createPATRequest : CreatePATRequest =  // CreatePATRequest | 
try {
    val result : CreatePATResponse = apiInstance.createPersonalAccessToken(createPATRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PersonalAccessTokensApi#createPersonalAccessToken")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PersonalAccessTokensApi#createPersonalAccessToken")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createPATRequest** | [**CreatePATRequest**](CreatePATRequest.md)|  | |

### Return type

[**CreatePATResponse**](CreatePATResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="listAvailablePATScopes"></a>
# **listAvailablePATScopes**
> PATScopesResponse listAvailablePATScopes()

List the scope strings PATs can be issued with.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PersonalAccessTokensApi()
try {
    val result : PATScopesResponse = apiInstance.listAvailablePATScopes()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PersonalAccessTokensApi#listAvailablePATScopes")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PersonalAccessTokensApi#listAvailablePATScopes")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PATScopesResponse**](PATScopesResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listPersonalAccessTokens"></a>
# **listPersonalAccessTokens**
> PATListResponse listPersonalAccessTokens()

List the caller&#39;s personal access tokens (with available scopes).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PersonalAccessTokensApi()
try {
    val result : PATListResponse = apiInstance.listPersonalAccessTokens()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PersonalAccessTokensApi#listPersonalAccessTokens")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PersonalAccessTokensApi#listPersonalAccessTokens")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PATListResponse**](PATListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="revokePersonalAccessToken"></a>
# **revokePersonalAccessToken**
> revokePersonalAccessToken(id)

Revoke a PAT.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PersonalAccessTokensApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.revokePersonalAccessToken(id)
} catch (e: ClientException) {
    println("4xx response calling PersonalAccessTokensApi#revokePersonalAccessToken")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PersonalAccessTokensApi#revokePersonalAccessToken")
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

<a id="updatePersonalAccessToken"></a>
# **updatePersonalAccessToken**
> PersonalAccessToken updatePersonalAccessToken(id, updatePATRequest)

Rename or re-describe a PAT (scopes are immutable).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PersonalAccessTokensApi()
val id : kotlin.String = id_example // kotlin.String | 
val updatePATRequest : UpdatePATRequest =  // UpdatePATRequest | 
try {
    val result : PersonalAccessToken = apiInstance.updatePersonalAccessToken(id, updatePATRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PersonalAccessTokensApi#updatePersonalAccessToken")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PersonalAccessTokensApi#updatePersonalAccessToken")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updatePATRequest** | [**UpdatePATRequest**](UpdatePATRequest.md)|  | |

### Return type

[**PersonalAccessToken**](PersonalAccessToken.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceCreatePAT"></a>
# **workspaceCreatePAT**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreatePAT(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PersonalAccessTokensApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreatePAT(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PersonalAccessTokensApi#workspaceCreatePAT")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PersonalAccessTokensApi#workspaceCreatePAT")
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

<a id="workspaceListPATs"></a>
# **workspaceListPATs**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListPATs(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PersonalAccessTokensApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListPATs(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PersonalAccessTokensApi#workspaceListPATs")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PersonalAccessTokensApi#workspaceListPATs")
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

<a id="workspaceRevokePAT"></a>
# **workspaceRevokePAT**
> workspaceRevokePAT(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PersonalAccessTokensApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceRevokePAT(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling PersonalAccessTokensApi#workspaceRevokePAT")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PersonalAccessTokensApi#workspaceRevokePAT")
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

<a id="workspaceUpdatePAT"></a>
# **workspaceUpdatePAT**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUpdatePAT(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PersonalAccessTokensApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUpdatePAT(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PersonalAccessTokensApi#workspaceUpdatePAT")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PersonalAccessTokensApi#workspaceUpdatePAT")
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

