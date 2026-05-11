# AccountApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**changePassword**](AccountApi.md#changePassword) | **POST** /v1/account/security/password | Change or set the account password. |
| [**consumeAgentTask**](AccountApi.md#consumeAgentTask) | **POST** /v1/account/usage/consume-agent-task | Atomic check + increment on the agent-task counter (one slot per turn). |
| [**getAccountPlan**](AccountApi.md#getAccountPlan) | **GET** /v1/account/plan | The caller&#39;s subscription tier and status. |
| [**getAccountTier**](AccountApi.md#getAccountTier) | **GET** /v1/account/tier | Capability + quota envelope for the caller&#39;s tier. |
| [**getAccountUsage**](AccountApi.md#getAccountUsage) | **GET** /v1/account/usage | Today&#39;s usage counters across notes, sheets, slides, files, tasks, mail, API. |
| [**getAgentTaskUsage**](AccountApi.md#getAgentTaskUsage) | **GET** /v1/account/usage/agent-tasks | Free-trial agent-task counter snapshot. Read-only; does NOT consume a slot. Use POST &#x60;/v1/account/usage/consume-agent-task&#x60; atomically per turn to gate a tool-using turn.  |
| [**getSignInMethods**](AccountApi.md#getSignInMethods) | **GET** /v1/account/security/sign-in-methods | List the linked sign-in methods (password + OAuth providers). |
| [**listConnectedApps**](AccountApi.md#listConnectedApps) | **GET** /v1/account/connected-apps | List the OAuth clients the calling user has granted access to. |
| [**listSessions**](AccountApi.md#listSessions) | **GET** /v1/account/security/sessions | List active sessions for the caller. |
| [**revokeConnectedApp**](AccountApi.md#revokeConnectedApp) | **DELETE** /v1/account/connected-apps/{client_id} | Revoke a connected app and all of its active tokens. |
| [**revokeOtherSessions**](AccountApi.md#revokeOtherSessions) | **POST** /v1/account/security/sessions/revoke-others | Revoke every session except the caller&#39;s current one. |
| [**revokeSession**](AccountApi.md#revokeSession) | **DELETE** /v1/account/security/sessions/{id} | Revoke a specific session. |


<a id="changePassword"></a>
# **changePassword**
> changePassword(changePasswordRequest)

Change or set the account password.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AccountApi()
val changePasswordRequest : ChangePasswordRequest =  // ChangePasswordRequest | 
try {
    apiInstance.changePassword(changePasswordRequest)
} catch (e: ClientException) {
    println("4xx response calling AccountApi#changePassword")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AccountApi#changePassword")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **changePasswordRequest** | [**ChangePasswordRequest**](ChangePasswordRequest.md)|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="consumeAgentTask"></a>
# **consumeAgentTask**
> ConsumeAgentTaskResponse consumeAgentTask()

Atomic check + increment on the agent-task counter (one slot per turn).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AccountApi()
try {
    val result : ConsumeAgentTaskResponse = apiInstance.consumeAgentTask()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AccountApi#consumeAgentTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AccountApi#consumeAgentTask")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ConsumeAgentTaskResponse**](ConsumeAgentTaskResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getAccountPlan"></a>
# **getAccountPlan**
> AccountPlan getAccountPlan()

The caller&#39;s subscription tier and status.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AccountApi()
try {
    val result : AccountPlan = apiInstance.getAccountPlan()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AccountApi#getAccountPlan")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AccountApi#getAccountPlan")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AccountPlan**](AccountPlan.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getAccountTier"></a>
# **getAccountTier**
> AccountTierDetails getAccountTier()

Capability + quota envelope for the caller&#39;s tier.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AccountApi()
try {
    val result : AccountTierDetails = apiInstance.getAccountTier()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AccountApi#getAccountTier")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AccountApi#getAccountTier")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AccountTierDetails**](AccountTierDetails.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getAccountUsage"></a>
# **getAccountUsage**
> AccountUsage getAccountUsage()

Today&#39;s usage counters across notes, sheets, slides, files, tasks, mail, API.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AccountApi()
try {
    val result : AccountUsage = apiInstance.getAccountUsage()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AccountApi#getAccountUsage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AccountApi#getAccountUsage")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AccountUsage**](AccountUsage.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getAgentTaskUsage"></a>
# **getAgentTaskUsage**
> AgentTaskUsage getAgentTaskUsage()

Free-trial agent-task counter snapshot. Read-only; does NOT consume a slot. Use POST &#x60;/v1/account/usage/consume-agent-task&#x60; atomically per turn to gate a tool-using turn. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AccountApi()
try {
    val result : AgentTaskUsage = apiInstance.getAgentTaskUsage()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AccountApi#getAgentTaskUsage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AccountApi#getAgentTaskUsage")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AgentTaskUsage**](AgentTaskUsage.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getSignInMethods"></a>
# **getSignInMethods**
> SignInMethods getSignInMethods()

List the linked sign-in methods (password + OAuth providers).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AccountApi()
try {
    val result : SignInMethods = apiInstance.getSignInMethods()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AccountApi#getSignInMethods")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AccountApi#getSignInMethods")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**SignInMethods**](SignInMethods.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listConnectedApps"></a>
# **listConnectedApps**
> ConnectedAppsListResponse listConnectedApps()

List the OAuth clients the calling user has granted access to.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AccountApi()
try {
    val result : ConnectedAppsListResponse = apiInstance.listConnectedApps()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AccountApi#listConnectedApps")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AccountApi#listConnectedApps")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ConnectedAppsListResponse**](ConnectedAppsListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listSessions"></a>
# **listSessions**
> SessionListResponse listSessions()

List active sessions for the caller.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AccountApi()
try {
    val result : SessionListResponse = apiInstance.listSessions()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AccountApi#listSessions")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AccountApi#listSessions")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**SessionListResponse**](SessionListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="revokeConnectedApp"></a>
# **revokeConnectedApp**
> revokeConnectedApp(clientId)

Revoke a connected app and all of its active tokens.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AccountApi()
val clientId : kotlin.String = clientId_example // kotlin.String | 
try {
    apiInstance.revokeConnectedApp(clientId)
} catch (e: ClientException) {
    println("4xx response calling AccountApi#revokeConnectedApp")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AccountApi#revokeConnectedApp")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **clientId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a id="revokeOtherSessions"></a>
# **revokeOtherSessions**
> RevokeOtherSessionsResponse revokeOtherSessions()

Revoke every session except the caller&#39;s current one.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AccountApi()
try {
    val result : RevokeOtherSessionsResponse = apiInstance.revokeOtherSessions()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AccountApi#revokeOtherSessions")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AccountApi#revokeOtherSessions")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**RevokeOtherSessionsResponse**](RevokeOtherSessionsResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="revokeSession"></a>
# **revokeSession**
> revokeSession(id)

Revoke a specific session.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AccountApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.revokeSession(id)
} catch (e: ClientException) {
    println("4xx response calling AccountApi#revokeSession")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AccountApi#revokeSession")
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

