# SettingsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**bulkUpdateSettings**](SettingsApi.md#bulkUpdateSettings) | **POST** /v1/settings/bulk-update | Bulk-update multiple settings rows in one round-trip. |
| [**deleteCurrentUserSettings**](SettingsApi.md#deleteCurrentUserSettings) | **DELETE** /v1/settings | Reset the caller&#39;s user-level settings. |
| [**getCurrentUserSettings**](SettingsApi.md#getCurrentUserSettings) | **GET** /v1/settings | Fetch the caller&#39;s user-level settings. |
| [**getMailReadReceiptsPref**](SettingsApi.md#getMailReadReceiptsPref) | **GET** /v1/me/preferences/mail-read-receipts | Read the caller&#39;s mail-read-receipts preference. |
| [**getSettingsPermissions**](SettingsApi.md#getSettingsPermissions) | **GET** /v1/settings/permissions | Read the caller&#39;s settings-write permissions matrix. |
| [**getUserSettings**](SettingsApi.md#getUserSettings) | **GET** /v1/settings/user/{userId} | Fetch a specific user&#39;s settings (admin / self only). |
| [**getWorkspaceSettings**](SettingsApi.md#getWorkspaceSettings) | **GET** /v1/settings/workspace/{workspaceId} | Fetch workspace-level settings. |
| [**putCurrentUserSettings**](SettingsApi.md#putCurrentUserSettings) | **PUT** /v1/settings | Replace the caller&#39;s user-level settings. |
| [**putMailReadReceiptsPref**](SettingsApi.md#putMailReadReceiptsPref) | **PUT** /v1/me/preferences/mail-read-receipts | Update the caller&#39;s mail-read-receipts preference. |
| [**putUserSettings**](SettingsApi.md#putUserSettings) | **PUT** /v1/settings/user/{userId} | Replace a specific user&#39;s settings. |
| [**putWorkspaceSettings**](SettingsApi.md#putWorkspaceSettings) | **PUT** /v1/settings/workspace/{workspaceId} | Replace workspace-level settings. |


<a id="bulkUpdateSettings"></a>
# **bulkUpdateSettings**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; bulkUpdateSettings(requestBody)

Bulk-update multiple settings rows in one round-trip.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SettingsApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.bulkUpdateSettings(requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SettingsApi#bulkUpdateSettings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SettingsApi#bulkUpdateSettings")
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

<a id="deleteCurrentUserSettings"></a>
# **deleteCurrentUserSettings**
> deleteCurrentUserSettings()

Reset the caller&#39;s user-level settings.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SettingsApi()
try {
    apiInstance.deleteCurrentUserSettings()
} catch (e: ClientException) {
    println("4xx response calling SettingsApi#deleteCurrentUserSettings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SettingsApi#deleteCurrentUserSettings")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getCurrentUserSettings"></a>
# **getCurrentUserSettings**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getCurrentUserSettings()

Fetch the caller&#39;s user-level settings.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SettingsApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getCurrentUserSettings()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SettingsApi#getCurrentUserSettings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SettingsApi#getCurrentUserSettings")
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

<a id="getMailReadReceiptsPref"></a>
# **getMailReadReceiptsPref**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getMailReadReceiptsPref()

Read the caller&#39;s mail-read-receipts preference.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SettingsApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getMailReadReceiptsPref()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SettingsApi#getMailReadReceiptsPref")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SettingsApi#getMailReadReceiptsPref")
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

<a id="getSettingsPermissions"></a>
# **getSettingsPermissions**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getSettingsPermissions()

Read the caller&#39;s settings-write permissions matrix.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SettingsApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getSettingsPermissions()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SettingsApi#getSettingsPermissions")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SettingsApi#getSettingsPermissions")
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

<a id="getUserSettings"></a>
# **getUserSettings**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getUserSettings(userId)

Fetch a specific user&#39;s settings (admin / self only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SettingsApi()
val userId : kotlin.String = userId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getUserSettings(userId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SettingsApi#getUserSettings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SettingsApi#getUserSettings")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **userId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getWorkspaceSettings"></a>
# **getWorkspaceSettings**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getWorkspaceSettings(workspaceId)

Fetch workspace-level settings.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SettingsApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getWorkspaceSettings(workspaceId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SettingsApi#getWorkspaceSettings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SettingsApi#getWorkspaceSettings")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspaceId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="putCurrentUserSettings"></a>
# **putCurrentUserSettings**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; putCurrentUserSettings(requestBody)

Replace the caller&#39;s user-level settings.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SettingsApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.putCurrentUserSettings(requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SettingsApi#putCurrentUserSettings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SettingsApi#putCurrentUserSettings")
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

<a id="putMailReadReceiptsPref"></a>
# **putMailReadReceiptsPref**
> putMailReadReceiptsPref(requestBody)

Update the caller&#39;s mail-read-receipts preference.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SettingsApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    apiInstance.putMailReadReceiptsPref(requestBody)
} catch (e: ClientException) {
    println("4xx response calling SettingsApi#putMailReadReceiptsPref")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SettingsApi#putMailReadReceiptsPref")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **requestBody** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="putUserSettings"></a>
# **putUserSettings**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; putUserSettings(userId, requestBody)

Replace a specific user&#39;s settings.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SettingsApi()
val userId : kotlin.String = userId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.putUserSettings(userId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SettingsApi#putUserSettings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SettingsApi#putUserSettings")
    e.printStackTrace()
}
```

### Parameters
| **userId** | **kotlin.String**|  | |
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

<a id="putWorkspaceSettings"></a>
# **putWorkspaceSettings**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; putWorkspaceSettings(workspaceId, requestBody)

Replace workspace-level settings.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SettingsApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.putWorkspaceSettings(workspaceId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SettingsApi#putWorkspaceSettings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SettingsApi#putWorkspaceSettings")
    e.printStackTrace()
}
```

### Parameters
| **workspaceId** | **kotlin.String**|  | |
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

