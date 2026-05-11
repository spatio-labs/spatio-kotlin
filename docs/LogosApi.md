# LogosApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getDomainLogo**](LogosApi.md#getDomainLogo) | **GET** /v1/logos/domain/{domain} | Resolve a domain to its logo URL (CDN-cached 24h). |
| [**getEmailLogo**](LogosApi.md#getEmailLogo) | **GET** /v1/logos/email/{email} | Resolve an email address to its domain logo URL. |
| [**getLogosBatch**](LogosApi.md#getLogosBatch) | **POST** /v1/logos/batch | Batch-resolve a list of domains/emails to logo URLs in one call. |


<a id="getDomainLogo"></a>
# **getDomainLogo**
> GetDomainLogo200Response getDomainLogo(domain)

Resolve a domain to its logo URL (CDN-cached 24h).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = LogosApi()
val domain : kotlin.String = domain_example // kotlin.String | 
try {
    val result : GetDomainLogo200Response = apiInstance.getDomainLogo(domain)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling LogosApi#getDomainLogo")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling LogosApi#getDomainLogo")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **kotlin.String**|  | |

### Return type

[**GetDomainLogo200Response**](GetDomainLogo200Response.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getEmailLogo"></a>
# **getEmailLogo**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getEmailLogo(email)

Resolve an email address to its domain logo URL.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = LogosApi()
val email : kotlin.String = email_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getEmailLogo(email)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling LogosApi#getEmailLogo")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling LogosApi#getEmailLogo")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **email** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getLogosBatch"></a>
# **getLogosBatch**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getLogosBatch(requestBody)

Batch-resolve a list of domains/emails to logo URLs in one call.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = LogosApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getLogosBatch(requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling LogosApi#getLogosBatch")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling LogosApi#getLogosBatch")
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

