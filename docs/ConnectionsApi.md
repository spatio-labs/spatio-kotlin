# ConnectionsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**disconnectConnection**](ConnectionsApi.md#disconnectConnection) | **POST** /v1/connections/disconnect | Disconnect a connected account. |
| [**installConnection**](ConnectionsApi.md#installConnection) | **POST** /v1/connections/install | Begin an OAuth install for a connection. |
| [**listAccounts**](ConnectionsApi.md#listAccounts) | **GET** /v1/accounts | List the caller&#39;s multi-provider accounts. |
| [**listConnectionIntegrations**](ConnectionsApi.md#listConnectionIntegrations) | **GET** /v1/connections/integrations | List supported integrations + their connection state. Legacy path; &#x60;/v1/connections/list&#x60; is the preferred alias.  |
| [**listConnections**](ConnectionsApi.md#listConnections) | **GET** /v1/connections/list | List supported integrations + their connection state. |
| [**listUserConnections**](ConnectionsApi.md#listUserConnections) | **GET** /v1/connections/user | List the caller&#39;s connected accounts. |
| [**refreshConnection**](ConnectionsApi.md#refreshConnection) | **POST** /v1/connections/refresh | Force a refresh of a connection&#39;s OAuth tokens. |
| [**removeAccount**](ConnectionsApi.md#removeAccount) | **DELETE** /v1/accounts/{accountId} | Remove an account. |
| [**resolveAccount**](ConnectionsApi.md#resolveAccount) | **GET** /v1/accounts/resolve | Resolve an account by provider/identifier. |
| [**syncAccount**](ConnectionsApi.md#syncAccount) | **POST** /v1/accounts/{accountId}/sync | Force a sync against the upstream provider. |
| [**updateAccount**](ConnectionsApi.md#updateAccount) | **PATCH** /v1/accounts/{accountId} | Update account metadata (label, etc.). |


<a id="disconnectConnection"></a>
# **disconnectConnection**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; disconnectConnection(disconnectConnectionRequest)

Disconnect a connected account.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConnectionsApi()
val disconnectConnectionRequest : DisconnectConnectionRequest =  // DisconnectConnectionRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.disconnectConnection(disconnectConnectionRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConnectionsApi#disconnectConnection")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConnectionsApi#disconnectConnection")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **disconnectConnectionRequest** | [**DisconnectConnectionRequest**](DisconnectConnectionRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="installConnection"></a>
# **installConnection**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; installConnection(installConnectionRequest)

Begin an OAuth install for a connection.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConnectionsApi()
val installConnectionRequest : InstallConnectionRequest =  // InstallConnectionRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.installConnection(installConnectionRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConnectionsApi#installConnection")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConnectionsApi#installConnection")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **installConnectionRequest** | [**InstallConnectionRequest**](InstallConnectionRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="listAccounts"></a>
# **listAccounts**
> AccountListResponse listAccounts()

List the caller&#39;s multi-provider accounts.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConnectionsApi()
try {
    val result : AccountListResponse = apiInstance.listAccounts()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConnectionsApi#listAccounts")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConnectionsApi#listAccounts")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AccountListResponse**](AccountListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listConnectionIntegrations"></a>
# **listConnectionIntegrations**
> ConnectionListResponse listConnectionIntegrations()

List supported integrations + their connection state. Legacy path; &#x60;/v1/connections/list&#x60; is the preferred alias. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConnectionsApi()
try {
    val result : ConnectionListResponse = apiInstance.listConnectionIntegrations()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConnectionsApi#listConnectionIntegrations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConnectionsApi#listConnectionIntegrations")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ConnectionListResponse**](ConnectionListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listConnections"></a>
# **listConnections**
> ConnectionListResponse listConnections()

List supported integrations + their connection state.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConnectionsApi()
try {
    val result : ConnectionListResponse = apiInstance.listConnections()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConnectionsApi#listConnections")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConnectionsApi#listConnections")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ConnectionListResponse**](ConnectionListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listUserConnections"></a>
# **listUserConnections**
> ConnectionAccountListResponse listUserConnections()

List the caller&#39;s connected accounts.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConnectionsApi()
try {
    val result : ConnectionAccountListResponse = apiInstance.listUserConnections()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConnectionsApi#listUserConnections")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConnectionsApi#listUserConnections")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ConnectionAccountListResponse**](ConnectionAccountListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="refreshConnection"></a>
# **refreshConnection**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; refreshConnection(refreshConnectionRequest)

Force a refresh of a connection&#39;s OAuth tokens.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConnectionsApi()
val refreshConnectionRequest : RefreshConnectionRequest =  // RefreshConnectionRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.refreshConnection(refreshConnectionRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConnectionsApi#refreshConnection")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConnectionsApi#refreshConnection")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **refreshConnectionRequest** | [**RefreshConnectionRequest**](RefreshConnectionRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="removeAccount"></a>
# **removeAccount**
> removeAccount(accountId)

Remove an account.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConnectionsApi()
val accountId : kotlin.String = accountId_example // kotlin.String | 
try {
    apiInstance.removeAccount(accountId)
} catch (e: ClientException) {
    println("4xx response calling ConnectionsApi#removeAccount")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConnectionsApi#removeAccount")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="resolveAccount"></a>
# **resolveAccount**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; resolveAccount(provider, email)

Resolve an account by provider/identifier.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConnectionsApi()
val provider : kotlin.String = provider_example // kotlin.String | 
val email : kotlin.String = email_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.resolveAccount(provider, email)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConnectionsApi#resolveAccount")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConnectionsApi#resolveAccount")
    e.printStackTrace()
}
```

### Parameters
| **provider** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **email** | **kotlin.String**|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="syncAccount"></a>
# **syncAccount**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; syncAccount(accountId)

Force a sync against the upstream provider.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConnectionsApi()
val accountId : kotlin.String = accountId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.syncAccount(accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConnectionsApi#syncAccount")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConnectionsApi#syncAccount")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateAccount"></a>
# **updateAccount**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateAccount(accountId, updateAccountRequest)

Update account metadata (label, etc.).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConnectionsApi()
val accountId : kotlin.String = accountId_example // kotlin.String | 
val updateAccountRequest : UpdateAccountRequest =  // UpdateAccountRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateAccount(accountId, updateAccountRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConnectionsApi#updateAccount")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConnectionsApi#updateAccount")
    e.printStackTrace()
}
```

### Parameters
| **accountId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateAccountRequest** | [**UpdateAccountRequest**](UpdateAccountRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

