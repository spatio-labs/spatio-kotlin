# PlatformsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addPlatformProviderAccount**](PlatformsApi.md#addPlatformProviderAccount) | **POST** /v1/platforms/{platformId}/providers/{provider}/accounts | Add a connected account for a platform/provider pair. |
| [**createOrUpdatePlatformSecret**](PlatformsApi.md#createOrUpdatePlatformSecret) | **POST** /v1/platforms/{platformId}/secrets | Create or update a secret value. |
| [**deletePlatformSecret**](PlatformsApi.md#deletePlatformSecret) | **DELETE** /v1/platforms/{platformId}/secrets/{name} | Delete a secret. |
| [**execPlatformData**](PlatformsApi.md#execPlatformData) | **POST** /v1/platforms/{platformId}/exec | Run an INSERT/UPDATE/DELETE statement against a platform&#39;s store. |
| [**exportPlatformSecrets**](PlatformsApi.md#exportPlatformSecrets) | **GET** /v1/platforms/{platformId}/secrets/export | Export all secrets for a platform (values included). Caller must be the platform owner.  |
| [**generatePlatformBackendToken**](PlatformsApi.md#generatePlatformBackendToken) | **POST** /v1/platforms/{platformId}/backend-token | Generate a short-lived backend JWT a platform&#39;s worker can use to call back into platform-service.  |
| [**getPlatformCatalog**](PlatformsApi.md#getPlatformCatalog) | **GET** /v1/catalog/platforms | List the global platform catalog — every platform that exists, not just the ones the caller has installed.  |
| [**getPlatformManifest**](PlatformsApi.md#getPlatformManifest) | **GET** /v1/platforms/{platformId}/manifest | Fetch a platform&#39;s manifest (capabilities, schema, UI metadata). |
| [**listPlatformAccounts**](PlatformsApi.md#listPlatformAccounts) | **GET** /v1/platforms/{platformId}/accounts | List accounts the caller has connected for a platform. |
| [**listPlatformProviders**](PlatformsApi.md#listPlatformProviders) | **GET** /v1/platforms/{platformId}/providers | Discover supported providers + capabilities for a platform. |
| [**listPlatformSecrets**](PlatformsApi.md#listPlatformSecrets) | **GET** /v1/platforms/{platformId}/secrets | List secret keys (values redacted). |
| [**listPlatformTables**](PlatformsApi.md#listPlatformTables) | **GET** /v1/platforms/{platformId}/tables | List tables in a platform&#39;s data store. |
| [**listPlatforms**](PlatformsApi.md#listPlatforms) | **GET** /v1/platforms | List installed platforms for the sidebar. |
| [**queryPlatformData**](PlatformsApi.md#queryPlatformData) | **POST** /v1/platforms/{platformId}/query | Run a SELECT query against a platform&#39;s data store. |
| [**runPlatformMigrations**](PlatformsApi.md#runPlatformMigrations) | **POST** /v1/platforms/{platformId}/migrate | Run pending migrations for a platform. |


<a id="addPlatformProviderAccount"></a>
# **addPlatformProviderAccount**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; addPlatformProviderAccount(platformId, provider, requestBody)

Add a connected account for a platform/provider pair.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
val provider : kotlin.String = provider_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.addPlatformProviderAccount(platformId, provider, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#addPlatformProviderAccount")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#addPlatformProviderAccount")
    e.printStackTrace()
}
```

### Parameters
| **platformId** | **kotlin.String**|  | |
| **provider** | **kotlin.String**|  | |
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

<a id="createOrUpdatePlatformSecret"></a>
# **createOrUpdatePlatformSecret**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; createOrUpdatePlatformSecret(platformId, requestBody)

Create or update a secret value.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.createOrUpdatePlatformSecret(platformId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#createOrUpdatePlatformSecret")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#createOrUpdatePlatformSecret")
    e.printStackTrace()
}
```

### Parameters
| **platformId** | **kotlin.String**|  | |
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

<a id="deletePlatformSecret"></a>
# **deletePlatformSecret**
> deletePlatformSecret(platformId, name)

Delete a secret.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
val name : kotlin.String = name_example // kotlin.String | 
try {
    apiInstance.deletePlatformSecret(platformId, name)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#deletePlatformSecret")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#deletePlatformSecret")
    e.printStackTrace()
}
```

### Parameters
| **platformId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **name** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="execPlatformData"></a>
# **execPlatformData**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; execPlatformData(platformId, requestBody)

Run an INSERT/UPDATE/DELETE statement against a platform&#39;s store.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.execPlatformData(platformId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#execPlatformData")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#execPlatformData")
    e.printStackTrace()
}
```

### Parameters
| **platformId** | **kotlin.String**|  | |
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

<a id="exportPlatformSecrets"></a>
# **exportPlatformSecrets**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; exportPlatformSecrets(platformId)

Export all secrets for a platform (values included). Caller must be the platform owner. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.exportPlatformSecrets(platformId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#exportPlatformSecrets")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#exportPlatformSecrets")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platformId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="generatePlatformBackendToken"></a>
# **generatePlatformBackendToken**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; generatePlatformBackendToken(platformId)

Generate a short-lived backend JWT a platform&#39;s worker can use to call back into platform-service. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.generatePlatformBackendToken(platformId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#generatePlatformBackendToken")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#generatePlatformBackendToken")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platformId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getPlatformCatalog"></a>
# **getPlatformCatalog**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getPlatformCatalog()

List the global platform catalog — every platform that exists, not just the ones the caller has installed. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getPlatformCatalog()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#getPlatformCatalog")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#getPlatformCatalog")
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

<a id="getPlatformManifest"></a>
# **getPlatformManifest**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getPlatformManifest(platformId)

Fetch a platform&#39;s manifest (capabilities, schema, UI metadata).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getPlatformManifest(platformId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#getPlatformManifest")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#getPlatformManifest")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platformId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listPlatformAccounts"></a>
# **listPlatformAccounts**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listPlatformAccounts(platformId)

List accounts the caller has connected for a platform.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listPlatformAccounts(platformId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#listPlatformAccounts")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#listPlatformAccounts")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platformId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listPlatformProviders"></a>
# **listPlatformProviders**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listPlatformProviders(platformId)

Discover supported providers + capabilities for a platform.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listPlatformProviders(platformId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#listPlatformProviders")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#listPlatformProviders")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platformId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listPlatformSecrets"></a>
# **listPlatformSecrets**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listPlatformSecrets(platformId)

List secret keys (values redacted).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listPlatformSecrets(platformId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#listPlatformSecrets")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#listPlatformSecrets")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platformId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listPlatformTables"></a>
# **listPlatformTables**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listPlatformTables(platformId)

List tables in a platform&#39;s data store.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listPlatformTables(platformId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#listPlatformTables")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#listPlatformTables")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platformId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listPlatforms"></a>
# **listPlatforms**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listPlatforms()

List installed platforms for the sidebar.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listPlatforms()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#listPlatforms")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#listPlatforms")
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

<a id="queryPlatformData"></a>
# **queryPlatformData**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; queryPlatformData(platformId, requestBody)

Run a SELECT query against a platform&#39;s data store.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.queryPlatformData(platformId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#queryPlatformData")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#queryPlatformData")
    e.printStackTrace()
}
```

### Parameters
| **platformId** | **kotlin.String**|  | |
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

<a id="runPlatformMigrations"></a>
# **runPlatformMigrations**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; runPlatformMigrations(platformId)

Run pending migrations for a platform.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = PlatformsApi()
val platformId : kotlin.String = platformId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.runPlatformMigrations(platformId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PlatformsApi#runPlatformMigrations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PlatformsApi#runPlatformMigrations")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platformId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

