# KeybindingsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteKeyBinding**](KeybindingsApi.md#deleteKeyBinding) | **DELETE** /v1/keybindings/{id} | Reset a binding to its platform default. |
| [**getDefaultKeyBindings**](KeybindingsApi.md#getDefaultKeyBindings) | **GET** /v1/keybindings/defaults | Platform default key bindings (no user customizations applied). |
| [**listKeyBindings**](KeybindingsApi.md#listKeyBindings) | **GET** /v1/keybindings | User&#39;s merged key bindings (defaults + customizations). |
| [**resetAllKeyBindings**](KeybindingsApi.md#resetAllKeyBindings) | **POST** /v1/keybindings/reset | Reset every customization to its platform default. |
| [**updateKeyBinding**](KeybindingsApi.md#updateKeyBinding) | **PUT** /v1/keybindings/{id} | Create or update a user key-binding customization. |
| [**validateKeyBinding**](KeybindingsApi.md#validateKeyBinding) | **POST** /v1/keybindings/validate | Check whether a proposed binding conflicts with existing ones. |


<a id="deleteKeyBinding"></a>
# **deleteKeyBinding**
> deleteKeyBinding(id)

Reset a binding to its platform default.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = KeybindingsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteKeyBinding(id)
} catch (e: ClientException) {
    println("4xx response calling KeybindingsApi#deleteKeyBinding")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling KeybindingsApi#deleteKeyBinding")
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

<a id="getDefaultKeyBindings"></a>
# **getDefaultKeyBindings**
> KeyBindingListResponse getDefaultKeyBindings()

Platform default key bindings (no user customizations applied).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = KeybindingsApi()
try {
    val result : KeyBindingListResponse = apiInstance.getDefaultKeyBindings()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling KeybindingsApi#getDefaultKeyBindings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling KeybindingsApi#getDefaultKeyBindings")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**KeyBindingListResponse**](KeyBindingListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listKeyBindings"></a>
# **listKeyBindings**
> KeyBindingListResponse listKeyBindings()

User&#39;s merged key bindings (defaults + customizations).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = KeybindingsApi()
try {
    val result : KeyBindingListResponse = apiInstance.listKeyBindings()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling KeybindingsApi#listKeyBindings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling KeybindingsApi#listKeyBindings")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**KeyBindingListResponse**](KeyBindingListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="resetAllKeyBindings"></a>
# **resetAllKeyBindings**
> resetAllKeyBindings()

Reset every customization to its platform default.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = KeybindingsApi()
try {
    apiInstance.resetAllKeyBindings()
} catch (e: ClientException) {
    println("4xx response calling KeybindingsApi#resetAllKeyBindings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling KeybindingsApi#resetAllKeyBindings")
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

<a id="updateKeyBinding"></a>
# **updateKeyBinding**
> KeyBinding updateKeyBinding(id, updateKeyBindingRequest)

Create or update a user key-binding customization.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = KeybindingsApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateKeyBindingRequest : UpdateKeyBindingRequest =  // UpdateKeyBindingRequest | 
try {
    val result : KeyBinding = apiInstance.updateKeyBinding(id, updateKeyBindingRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling KeybindingsApi#updateKeyBinding")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling KeybindingsApi#updateKeyBinding")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateKeyBindingRequest** | [**UpdateKeyBindingRequest**](UpdateKeyBindingRequest.md)|  | |

### Return type

[**KeyBinding**](KeyBinding.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="validateKeyBinding"></a>
# **validateKeyBinding**
> ValidateKeyBindingResponse validateKeyBinding(validateKeyBindingRequest)

Check whether a proposed binding conflicts with existing ones.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = KeybindingsApi()
val validateKeyBindingRequest : ValidateKeyBindingRequest =  // ValidateKeyBindingRequest | 
try {
    val result : ValidateKeyBindingResponse = apiInstance.validateKeyBinding(validateKeyBindingRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling KeybindingsApi#validateKeyBinding")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling KeybindingsApi#validateKeyBinding")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **validateKeyBindingRequest** | [**ValidateKeyBindingRequest**](ValidateKeyBindingRequest.md)|  | |

### Return type

[**ValidateKeyBindingResponse**](ValidateKeyBindingResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

