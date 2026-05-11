# MiscApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deletePinnedPlatform**](MiscApi.md#deletePinnedPlatform) | **DELETE** /v1/pinned-platforms/{platformId} | Unpin a platform. |
| [**getBootstrap**](MiscApi.md#getBootstrap) | **GET** /v1/bootstrap | Single-shot identity + config bundle the renderer hits on first load. Replaces the legacy server-side hydration in app/layout.tsx.  |
| [**getOnboardingInvitations**](MiscApi.md#getOnboardingInvitations) | **GET** /v1/onboarding/invitations | Pending invitations the caller can accept during onboarding. |
| [**getPinnedPlatforms**](MiscApi.md#getPinnedPlatforms) | **GET** /v1/pinned-platforms | Read the caller&#39;s pinned-platform list (sidebar order). |
| [**getPlatformPreferences**](MiscApi.md#getPlatformPreferences) | **GET** /v1/platform-preferences | Read the caller&#39;s per-platform sidebar/visibility preferences. |
| [**getPlatformSettingsLegacy**](MiscApi.md#getPlatformSettingsLegacy) | **GET** /v1/settings/platform | Legacy admin-tier platform settings read endpoint. |
| [**getThreadsStatus**](MiscApi.md#getThreadsStatus) | **GET** /v1/threads/status | Async-thread / job-runner status snapshot. |
| [**getUserPermissions**](MiscApi.md#getUserPermissions) | **GET** /v1/user/permissions | Read the caller&#39;s effective per-resource permissions. |
| [**getWorkspaceActivity**](MiscApi.md#getWorkspaceActivity) | **GET** /v1/workspace-activity | Recent activity feed for a workspace. |
| [**getWorkspaceLayout**](MiscApi.md#getWorkspaceLayout) | **GET** /v1/layout/{workspaceId} | Read the renderer&#39;s saved pane layout for a workspace. |
| [**putPinnedPlatform**](MiscApi.md#putPinnedPlatform) | **PUT** /v1/pinned-platforms | Pin a platform. |
| [**putPlatformPreferences**](MiscApi.md#putPlatformPreferences) | **PUT** /v1/platform-preferences | Replace the caller&#39;s platform preferences. |
| [**putWorkspaceLayout**](MiscApi.md#putWorkspaceLayout) | **PUT** /v1/layout/{workspaceId} | Save the renderer&#39;s pane layout. |
| [**reorderPinnedPlatforms**](MiscApi.md#reorderPinnedPlatforms) | **POST** /v1/pinned-platforms/reorder | Reorder the pinned-platform list. |
| [**resetPlatformPreferences**](MiscApi.md#resetPlatformPreferences) | **POST** /v1/platform-preferences/reset | Reset platform preferences to defaults. |
| [**updateUserProfile**](MiscApi.md#updateUserProfile) | **PATCH** /v1/user/profile | Update the caller&#39;s user profile (name, avatar, etc.). |
| [**validateOrganizationSlug**](MiscApi.md#validateOrganizationSlug) | **GET** /v1/validate-slug/organization | Check whether an org slug is available. |
| [**validateWorkspaceSlug**](MiscApi.md#validateWorkspaceSlug) | **GET** /v1/validate-slug/workspace | Check whether a workspace slug is available. |


<a id="deletePinnedPlatform"></a>
# **deletePinnedPlatform**
> deletePinnedPlatform(platformId)

Unpin a platform.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
try {
    apiInstance.deletePinnedPlatform(platformId)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#deletePinnedPlatform")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#deletePinnedPlatform")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platformId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getBootstrap"></a>
# **getBootstrap**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getBootstrap()

Single-shot identity + config bundle the renderer hits on first load. Replaces the legacy server-side hydration in app/layout.tsx. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getBootstrap()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#getBootstrap")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#getBootstrap")
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

<a id="getOnboardingInvitations"></a>
# **getOnboardingInvitations**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getOnboardingInvitations()

Pending invitations the caller can accept during onboarding.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getOnboardingInvitations()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#getOnboardingInvitations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#getOnboardingInvitations")
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

<a id="getPinnedPlatforms"></a>
# **getPinnedPlatforms**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getPinnedPlatforms()

Read the caller&#39;s pinned-platform list (sidebar order).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getPinnedPlatforms()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#getPinnedPlatforms")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#getPinnedPlatforms")
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

<a id="getPlatformPreferences"></a>
# **getPlatformPreferences**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getPlatformPreferences()

Read the caller&#39;s per-platform sidebar/visibility preferences.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getPlatformPreferences()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#getPlatformPreferences")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#getPlatformPreferences")
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

<a id="getPlatformSettingsLegacy"></a>
# **getPlatformSettingsLegacy**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getPlatformSettingsLegacy()

Legacy admin-tier platform settings read endpoint.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getPlatformSettingsLegacy()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#getPlatformSettingsLegacy")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#getPlatformSettingsLegacy")
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

<a id="getThreadsStatus"></a>
# **getThreadsStatus**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getThreadsStatus()

Async-thread / job-runner status snapshot.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getThreadsStatus()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#getThreadsStatus")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#getThreadsStatus")
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

<a id="getUserPermissions"></a>
# **getUserPermissions**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getUserPermissions()

Read the caller&#39;s effective per-resource permissions.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getUserPermissions()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#getUserPermissions")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#getUserPermissions")
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

<a id="getWorkspaceActivity"></a>
# **getWorkspaceActivity**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getWorkspaceActivity(workspaceId, limit)

Recent activity feed for a workspace.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val limit : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getWorkspaceActivity(workspaceId, limit)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#getWorkspaceActivity")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#getWorkspaceActivity")
    e.printStackTrace()
}
```

### Parameters
| **workspaceId** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **kotlin.Int**|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getWorkspaceLayout"></a>
# **getWorkspaceLayout**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getWorkspaceLayout(workspaceId)

Read the renderer&#39;s saved pane layout for a workspace.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getWorkspaceLayout(workspaceId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#getWorkspaceLayout")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#getWorkspaceLayout")
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

<a id="putPinnedPlatform"></a>
# **putPinnedPlatform**
> putPinnedPlatform(requestBody)

Pin a platform.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    apiInstance.putPinnedPlatform(requestBody)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#putPinnedPlatform")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#putPinnedPlatform")
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

<a id="putPlatformPreferences"></a>
# **putPlatformPreferences**
> putPlatformPreferences(requestBody)

Replace the caller&#39;s platform preferences.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    apiInstance.putPlatformPreferences(requestBody)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#putPlatformPreferences")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#putPlatformPreferences")
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

<a id="putWorkspaceLayout"></a>
# **putWorkspaceLayout**
> putWorkspaceLayout(workspaceId, requestBody)

Save the renderer&#39;s pane layout.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    apiInstance.putWorkspaceLayout(workspaceId, requestBody)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#putWorkspaceLayout")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#putWorkspaceLayout")
    e.printStackTrace()
}
```

### Parameters
| **workspaceId** | **kotlin.String**|  | |
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

<a id="reorderPinnedPlatforms"></a>
# **reorderPinnedPlatforms**
> reorderPinnedPlatforms(requestBody)

Reorder the pinned-platform list.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    apiInstance.reorderPinnedPlatforms(requestBody)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#reorderPinnedPlatforms")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#reorderPinnedPlatforms")
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

<a id="resetPlatformPreferences"></a>
# **resetPlatformPreferences**
> resetPlatformPreferences()

Reset platform preferences to defaults.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
try {
    apiInstance.resetPlatformPreferences()
} catch (e: ClientException) {
    println("4xx response calling MiscApi#resetPlatformPreferences")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#resetPlatformPreferences")
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

<a id="updateUserProfile"></a>
# **updateUserProfile**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateUserProfile(requestBody)

Update the caller&#39;s user profile (name, avatar, etc.).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateUserProfile(requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#updateUserProfile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#updateUserProfile")
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

<a id="validateOrganizationSlug"></a>
# **validateOrganizationSlug**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; validateOrganizationSlug(slug)

Check whether an org slug is available.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
val slug : kotlin.String = slug_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.validateOrganizationSlug(slug)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#validateOrganizationSlug")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#validateOrganizationSlug")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **slug** | **kotlin.String**|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="validateWorkspaceSlug"></a>
# **validateWorkspaceSlug**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; validateWorkspaceSlug(slug, organizationId)

Check whether a workspace slug is available.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MiscApi()
val slug : kotlin.String = slug_example // kotlin.String | 
val organizationId : kotlin.String = organizationId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.validateWorkspaceSlug(slug, organizationId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MiscApi#validateWorkspaceSlug")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MiscApi#validateWorkspaceSlug")
    e.printStackTrace()
}
```

### Parameters
| **slug** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organizationId** | **kotlin.String**|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

