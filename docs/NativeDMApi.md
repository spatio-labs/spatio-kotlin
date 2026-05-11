# NativeDMApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addNativeDMReaction**](NativeDMApi.md#addNativeDMReaction) | **POST** /v1/native/dm/messages/{messageId}/reactions | Add a reaction to a DM message. |
| [**attachToNativeDMMessage**](NativeDMApi.md#attachToNativeDMMessage) | **POST** /v1/native/dm/messages/{messageId}/attachments | Attach a file to a DM message. |
| [**deleteNativeDMMessage**](NativeDMApi.md#deleteNativeDMMessage) | **DELETE** /v1/native/dm/{dmId}/messages/{messageId} | Delete a DM message. |
| [**forwardNativeDMMessage**](NativeDMApi.md#forwardNativeDMMessage) | **POST** /v1/native/dm/messages/{messageId}/forward | Forward a DM message to another conversation. |
| [**listNativeDMChannels**](NativeDMApi.md#listNativeDMChannels) | **GET** /v1/native/dm | List the caller&#39;s DM channels. |
| [**listNativeDMConversations**](NativeDMApi.md#listNativeDMConversations) | **GET** /v1/native/dm/conversations | List DM conversations with metadata (last message, unread count, etc.). |
| [**listNativeDMMessages**](NativeDMApi.md#listNativeDMMessages) | **GET** /v1/native/dm/{dmId}/messages | List messages in a DM. |
| [**listNativeDMPinnedMessages**](NativeDMApi.md#listNativeDMPinnedMessages) | **GET** /v1/native/dm/{dmId}/pinned | List pinned messages in a DM. |
| [**listNativeDMThreadReplies**](NativeDMApi.md#listNativeDMThreadReplies) | **GET** /v1/native/dm/{dmId}/messages/{messageId}/replies | List threaded replies on a message. |
| [**markNativeDMRead**](NativeDMApi.md#markNativeDMRead) | **POST** /v1/native/dm/{dmId}/read | Mark a DM as read. |
| [**muteNativeDM**](NativeDMApi.md#muteNativeDM) | **POST** /v1/native/dm/{dmId}/mute | Mute a DM. |
| [**pinNativeDMConversation**](NativeDMApi.md#pinNativeDMConversation) | **POST** /v1/native/dm/{dmId}/pin | Pin a DM conversation in the sidebar. |
| [**pinNativeDMMessage**](NativeDMApi.md#pinNativeDMMessage) | **POST** /v1/native/dm/messages/{messageId}/pin | Pin a DM message. |
| [**postNativeDMMessage**](NativeDMApi.md#postNativeDMMessage) | **POST** /v1/native/dm | Post a DM message (top-level entry). |
| [**postNativeDMThreadReply**](NativeDMApi.md#postNativeDMThreadReply) | **POST** /v1/native/dm/{dmId}/messages/{messageId}/replies | Post a threaded reply. |
| [**removeNativeDMReaction**](NativeDMApi.md#removeNativeDMReaction) | **DELETE** /v1/native/dm/messages/{messageId}/reactions/{emoji} | Remove a reaction. |
| [**searchNativeDMMessages**](NativeDMApi.md#searchNativeDMMessages) | **GET** /v1/native/dm/search | Search DM messages. |
| [**setNativeDMDraft**](NativeDMApi.md#setNativeDMDraft) | **PUT** /v1/native/dm/{dmId}/draft | Save a draft on a DM conversation. |
| [**unpinNativeDMConversation**](NativeDMApi.md#unpinNativeDMConversation) | **DELETE** /v1/native/dm/{dmId}/pin | Unpin a DM conversation. |
| [**unpinNativeDMMessage**](NativeDMApi.md#unpinNativeDMMessage) | **DELETE** /v1/native/dm/messages/{messageId}/pin | Unpin a DM message. |
| [**updateNativeDMMessage**](NativeDMApi.md#updateNativeDMMessage) | **PATCH** /v1/native/dm/{dmId}/messages/{messageId} | Update a DM message body. |


<a id="addNativeDMReaction"></a>
# **addNativeDMReaction**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; addNativeDMReaction(messageId, requestBody)

Add a reaction to a DM message.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val messageId : kotlin.String = messageId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.addNativeDMReaction(messageId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#addNativeDMReaction")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#addNativeDMReaction")
    e.printStackTrace()
}
```

### Parameters
| **messageId** | **kotlin.String**|  | |
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

<a id="attachToNativeDMMessage"></a>
# **attachToNativeDMMessage**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; attachToNativeDMMessage(messageId, requestBody)

Attach a file to a DM message.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val messageId : kotlin.String = messageId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.attachToNativeDMMessage(messageId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#attachToNativeDMMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#attachToNativeDMMessage")
    e.printStackTrace()
}
```

### Parameters
| **messageId** | **kotlin.String**|  | |
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

<a id="deleteNativeDMMessage"></a>
# **deleteNativeDMMessage**
> deleteNativeDMMessage(dmId, messageId)

Delete a DM message.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val dmId : kotlin.String = dmId_example // kotlin.String | 
val messageId : kotlin.String = messageId_example // kotlin.String | 
try {
    apiInstance.deleteNativeDMMessage(dmId, messageId)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#deleteNativeDMMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#deleteNativeDMMessage")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **messageId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="forwardNativeDMMessage"></a>
# **forwardNativeDMMessage**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; forwardNativeDMMessage(messageId, requestBody)

Forward a DM message to another conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val messageId : kotlin.String = messageId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.forwardNativeDMMessage(messageId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#forwardNativeDMMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#forwardNativeDMMessage")
    e.printStackTrace()
}
```

### Parameters
| **messageId** | **kotlin.String**|  | |
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

<a id="listNativeDMChannels"></a>
# **listNativeDMChannels**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listNativeDMChannels()

List the caller&#39;s DM channels.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listNativeDMChannels()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#listNativeDMChannels")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#listNativeDMChannels")
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

<a id="listNativeDMConversations"></a>
# **listNativeDMConversations**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listNativeDMConversations()

List DM conversations with metadata (last message, unread count, etc.).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listNativeDMConversations()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#listNativeDMConversations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#listNativeDMConversations")
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

<a id="listNativeDMMessages"></a>
# **listNativeDMMessages**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listNativeDMMessages(dmId)

List messages in a DM.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val dmId : kotlin.String = dmId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listNativeDMMessages(dmId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#listNativeDMMessages")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#listNativeDMMessages")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dmId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listNativeDMPinnedMessages"></a>
# **listNativeDMPinnedMessages**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listNativeDMPinnedMessages(dmId)

List pinned messages in a DM.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val dmId : kotlin.String = dmId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listNativeDMPinnedMessages(dmId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#listNativeDMPinnedMessages")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#listNativeDMPinnedMessages")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dmId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listNativeDMThreadReplies"></a>
# **listNativeDMThreadReplies**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listNativeDMThreadReplies(dmId, messageId)

List threaded replies on a message.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val dmId : kotlin.String = dmId_example // kotlin.String | 
val messageId : kotlin.String = messageId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listNativeDMThreadReplies(dmId, messageId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#listNativeDMThreadReplies")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#listNativeDMThreadReplies")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **messageId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="markNativeDMRead"></a>
# **markNativeDMRead**
> markNativeDMRead(dmId)

Mark a DM as read.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val dmId : kotlin.String = dmId_example // kotlin.String | 
try {
    apiInstance.markNativeDMRead(dmId)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#markNativeDMRead")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#markNativeDMRead")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dmId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="muteNativeDM"></a>
# **muteNativeDM**
> muteNativeDM(dmId, requestBody)

Mute a DM.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val dmId : kotlin.String = dmId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    apiInstance.muteNativeDM(dmId, requestBody)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#muteNativeDM")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#muteNativeDM")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **requestBody** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="pinNativeDMConversation"></a>
# **pinNativeDMConversation**
> pinNativeDMConversation(dmId)

Pin a DM conversation in the sidebar.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val dmId : kotlin.String = dmId_example // kotlin.String | 
try {
    apiInstance.pinNativeDMConversation(dmId)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#pinNativeDMConversation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#pinNativeDMConversation")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dmId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="pinNativeDMMessage"></a>
# **pinNativeDMMessage**
> pinNativeDMMessage(messageId)

Pin a DM message.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val messageId : kotlin.String = messageId_example // kotlin.String | 
try {
    apiInstance.pinNativeDMMessage(messageId)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#pinNativeDMMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#pinNativeDMMessage")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **messageId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="postNativeDMMessage"></a>
# **postNativeDMMessage**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; postNativeDMMessage(requestBody)

Post a DM message (top-level entry).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.postNativeDMMessage(requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#postNativeDMMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#postNativeDMMessage")
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

<a id="postNativeDMThreadReply"></a>
# **postNativeDMThreadReply**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; postNativeDMThreadReply(dmId, messageId, requestBody)

Post a threaded reply.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val dmId : kotlin.String = dmId_example // kotlin.String | 
val messageId : kotlin.String = messageId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.postNativeDMThreadReply(dmId, messageId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#postNativeDMThreadReply")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#postNativeDMThreadReply")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**|  | |
| **messageId** | **kotlin.String**|  | |
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

<a id="removeNativeDMReaction"></a>
# **removeNativeDMReaction**
> removeNativeDMReaction(messageId, emoji)

Remove a reaction.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val messageId : kotlin.String = messageId_example // kotlin.String | 
val emoji : kotlin.String = emoji_example // kotlin.String | 
try {
    apiInstance.removeNativeDMReaction(messageId, emoji)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#removeNativeDMReaction")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#removeNativeDMReaction")
    e.printStackTrace()
}
```

### Parameters
| **messageId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **emoji** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="searchNativeDMMessages"></a>
# **searchNativeDMMessages**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; searchNativeDMMessages(q)

Search DM messages.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val q : kotlin.String = q_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.searchNativeDMMessages(q)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#searchNativeDMMessages")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#searchNativeDMMessages")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **kotlin.String**|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="setNativeDMDraft"></a>
# **setNativeDMDraft**
> setNativeDMDraft(dmId, requestBody)

Save a draft on a DM conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val dmId : kotlin.String = dmId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    apiInstance.setNativeDMDraft(dmId, requestBody)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#setNativeDMDraft")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#setNativeDMDraft")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**|  | |
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

<a id="unpinNativeDMConversation"></a>
# **unpinNativeDMConversation**
> unpinNativeDMConversation(dmId)

Unpin a DM conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val dmId : kotlin.String = dmId_example // kotlin.String | 
try {
    apiInstance.unpinNativeDMConversation(dmId)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#unpinNativeDMConversation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#unpinNativeDMConversation")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dmId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="unpinNativeDMMessage"></a>
# **unpinNativeDMMessage**
> unpinNativeDMMessage(messageId)

Unpin a DM message.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val messageId : kotlin.String = messageId_example // kotlin.String | 
try {
    apiInstance.unpinNativeDMMessage(messageId)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#unpinNativeDMMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#unpinNativeDMMessage")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **messageId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateNativeDMMessage"></a>
# **updateNativeDMMessage**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateNativeDMMessage(dmId, messageId, requestBody)

Update a DM message body.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NativeDMApi()
val dmId : kotlin.String = dmId_example // kotlin.String | 
val messageId : kotlin.String = messageId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateNativeDMMessage(dmId, messageId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NativeDMApi#updateNativeDMMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NativeDMApi#updateNativeDMMessage")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**|  | |
| **messageId** | **kotlin.String**|  | |
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

