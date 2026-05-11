# NotificationsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getNotificationPreferences**](NotificationsApi.md#getNotificationPreferences) | **GET** /v1/notifications/preferences | Read the caller&#39;s notification preferences. |
| [**updateNotificationPreferences**](NotificationsApi.md#updateNotificationPreferences) | **PATCH** /v1/notifications/preferences | Update notification preferences. |


<a id="getNotificationPreferences"></a>
# **getNotificationPreferences**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getNotificationPreferences()

Read the caller&#39;s notification preferences.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotificationsApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getNotificationPreferences()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotificationsApi#getNotificationPreferences")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotificationsApi#getNotificationPreferences")
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

<a id="updateNotificationPreferences"></a>
# **updateNotificationPreferences**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateNotificationPreferences(requestBody)

Update notification preferences.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotificationsApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateNotificationPreferences(requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotificationsApi#updateNotificationPreferences")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotificationsApi#updateNotificationPreferences")
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

