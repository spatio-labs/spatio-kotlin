# ConversationsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createConversation**](ConversationsApi.md#createConversation) | **POST** /v1/conversations | Persist a new LLM conversation. |
| [**deleteConversation**](ConversationsApi.md#deleteConversation) | **DELETE** /v1/conversations/{id} | Soft-delete a conversation. |
| [**getConversation**](ConversationsApi.md#getConversation) | **GET** /v1/conversations/{id} | Fetch one conversation. |
| [**getLatestConversationForContext**](ConversationsApi.md#getLatestConversationForContext) | **GET** /v1/conversations/latest | Fetch the most recently active conversation for a given context tag. |
| [**listConversationMessages**](ConversationsApi.md#listConversationMessages) | **GET** /v1/conversations/{id}/messages | List messages in a conversation. |
| [**listConversations**](ConversationsApi.md#listConversations) | **GET** /v1/conversations | List the caller&#39;s persisted LLM conversations. |
| [**saveConversationMessage**](ConversationsApi.md#saveConversationMessage) | **POST** /v1/conversations/{id}/messages | Append a message to a conversation. |
| [**updateConversation**](ConversationsApi.md#updateConversation) | **PATCH** /v1/conversations/{id} | Update conversation metadata (title, context, cwd, session_id, pinned). |
| [**updateConversationMessageMetadata**](ConversationsApi.md#updateConversationMessageMetadata) | **PATCH** /v1/conversations/{id}/messages | Patch metadata on an existing message. Body must include the message id (path is the conversation id, not the message).  |


<a id="createConversation"></a>
# **createConversation**
> Conversation createConversation(createConversationRequest)

Persist a new LLM conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConversationsApi()
val createConversationRequest : CreateConversationRequest =  // CreateConversationRequest | 
try {
    val result : Conversation = apiInstance.createConversation(createConversationRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConversationsApi#createConversation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConversationsApi#createConversation")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createConversationRequest** | [**CreateConversationRequest**](CreateConversationRequest.md)|  | [optional] |

### Return type

[**Conversation**](Conversation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteConversation"></a>
# **deleteConversation**
> deleteConversation(id)

Soft-delete a conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConversationsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteConversation(id)
} catch (e: ClientException) {
    println("4xx response calling ConversationsApi#deleteConversation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConversationsApi#deleteConversation")
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

<a id="getConversation"></a>
# **getConversation**
> Conversation getConversation(id)

Fetch one conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConversationsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : Conversation = apiInstance.getConversation(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConversationsApi#getConversation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConversationsApi#getConversation")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**Conversation**](Conversation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getLatestConversationForContext"></a>
# **getLatestConversationForContext**
> Conversation getLatestConversationForContext(context)

Fetch the most recently active conversation for a given context tag.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConversationsApi()
val context : kotlin.String = context_example // kotlin.String | 
try {
    val result : Conversation = apiInstance.getLatestConversationForContext(context)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConversationsApi#getLatestConversationForContext")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConversationsApi#getLatestConversationForContext")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **context** | **kotlin.String**|  | |

### Return type

[**Conversation**](Conversation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listConversationMessages"></a>
# **listConversationMessages**
> kotlin.collections.List&lt;ConversationMessage&gt; listConversationMessages(id, limit, before)

List messages in a conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConversationsApi()
val id : kotlin.String = id_example // kotlin.String | 
val limit : kotlin.Int = 56 // kotlin.Int | 
val before : kotlin.String = before_example // kotlin.String | 
try {
    val result : kotlin.collections.List<ConversationMessage> = apiInstance.listConversationMessages(id, limit, before)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConversationsApi#listConversationMessages")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConversationsApi#listConversationMessages")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| **limit** | **kotlin.Int**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **before** | **kotlin.String**|  | [optional] |

### Return type

[**kotlin.collections.List&lt;ConversationMessage&gt;**](ConversationMessage.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listConversations"></a>
# **listConversations**
> kotlin.collections.List&lt;Conversation&gt; listConversations(context, limit)

List the caller&#39;s persisted LLM conversations.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConversationsApi()
val context : kotlin.String = context_example // kotlin.String | 
val limit : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : kotlin.collections.List<Conversation> = apiInstance.listConversations(context, limit)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConversationsApi#listConversations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConversationsApi#listConversations")
    e.printStackTrace()
}
```

### Parameters
| **context** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **kotlin.Int**|  | [optional] |

### Return type

[**kotlin.collections.List&lt;Conversation&gt;**](Conversation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="saveConversationMessage"></a>
# **saveConversationMessage**
> ConversationMessage saveConversationMessage(id, saveMessageRequest)

Append a message to a conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConversationsApi()
val id : kotlin.String = id_example // kotlin.String | 
val saveMessageRequest : SaveMessageRequest =  // SaveMessageRequest | 
try {
    val result : ConversationMessage = apiInstance.saveConversationMessage(id, saveMessageRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConversationsApi#saveConversationMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConversationsApi#saveConversationMessage")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **saveMessageRequest** | [**SaveMessageRequest**](SaveMessageRequest.md)|  | |

### Return type

[**ConversationMessage**](ConversationMessage.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateConversation"></a>
# **updateConversation**
> Conversation updateConversation(id, updateConversationRequest)

Update conversation metadata (title, context, cwd, session_id, pinned).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConversationsApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateConversationRequest : UpdateConversationRequest =  // UpdateConversationRequest | 
try {
    val result : Conversation = apiInstance.updateConversation(id, updateConversationRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConversationsApi#updateConversation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConversationsApi#updateConversation")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateConversationRequest** | [**UpdateConversationRequest**](UpdateConversationRequest.md)|  | |

### Return type

[**Conversation**](Conversation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateConversationMessageMetadata"></a>
# **updateConversationMessageMetadata**
> ConversationMessage updateConversationMessageMetadata(id, updateMessageMetadataRequest)

Patch metadata on an existing message. Body must include the message id (path is the conversation id, not the message). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ConversationsApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateMessageMetadataRequest : UpdateMessageMetadataRequest =  // UpdateMessageMetadataRequest | 
try {
    val result : ConversationMessage = apiInstance.updateConversationMessageMetadata(id, updateMessageMetadataRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ConversationsApi#updateConversationMessageMetadata")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ConversationsApi#updateConversationMessageMetadata")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateMessageMetadataRequest** | [**UpdateMessageMetadataRequest**](UpdateMessageMetadataRequest.md)|  | |

### Return type

[**ConversationMessage**](ConversationMessage.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

