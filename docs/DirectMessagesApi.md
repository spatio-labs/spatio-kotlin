# DirectMessagesApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addDMReaction**](DirectMessagesApi.md#addDMReaction) | **POST** /v1/direct-messages/messages/{messageId}/reactions | React to a DM message. |
| [**attachToDMMessage**](DirectMessagesApi.md#attachToDMMessage) | **POST** /v1/direct-messages/messages/{messageId}/attachments | Attach a file/image/etc. to an existing DM message. |
| [**executeDMAction**](DirectMessagesApi.md#executeDMAction) | **POST** /v1/direct-messages/execute | Dispatch a DM action by id. |
| [**forwardDMMessage**](DirectMessagesApi.md#forwardDMMessage) | **POST** /v1/direct-messages/messages/{messageId}/forward | Forward a DM message to another DM or channel. |
| [**getDMUser**](DirectMessagesApi.md#getDMUser) | **GET** /v1/direct-messages/users/{id} | Fetch one chat user. |
| [**listDMActions**](DirectMessagesApi.md#listDMActions) | **GET** /v1/direct-messages/actions | Discover the action catalog for DirectMessages. |
| [**listDMPinnedMessages**](DirectMessagesApi.md#listDMPinnedMessages) | **GET** /v1/direct-messages/{dmId}/pinned | List pinned messages in a DM conversation. |
| [**listDMThreadReplies**](DirectMessagesApi.md#listDMThreadReplies) | **GET** /v1/direct-messages/{dmId}/messages/{messageId}/replies | List replies in a DM message thread. |
| [**listDMUsers**](DirectMessagesApi.md#listDMUsers) | **GET** /v1/direct-messages/users | List chat users (DM contacts) across connected accounts. |
| [**listDirectConversationsEnriched**](DirectMessagesApi.md#listDirectConversationsEnriched) | **GET** /v1/direct-messages/conversations | Enriched DM conversation list with unread + pin + draft state. |
| [**listDirectMessageConversations**](DirectMessagesApi.md#listDirectMessageConversations) | **GET** /v1/direct-messages | List 1:1 and group DM conversations. |
| [**listDirectMessages**](DirectMessagesApi.md#listDirectMessages) | **GET** /v1/direct-messages/messages | List messages in a DM conversation. |
| [**markDMRead**](DirectMessagesApi.md#markDMRead) | **POST** /v1/direct-messages/{dmId}/read | Mark a DM message read. |
| [**muteDM**](DirectMessagesApi.md#muteDM) | **POST** /v1/direct-messages/{dmId}/mute | Mute a DM conversation (until a time, or forever). |
| [**pinDMConversation**](DirectMessagesApi.md#pinDMConversation) | **POST** /v1/direct-messages/{dmId}/pin | Pin a DM conversation to the top of the sidebar. |
| [**pinDMMessage**](DirectMessagesApi.md#pinDMMessage) | **POST** /v1/direct-messages/messages/{messageId}/pin | Pin a DM message. |
| [**postDMThreadReply**](DirectMessagesApi.md#postDMThreadReply) | **POST** /v1/direct-messages/{dmId}/messages/{messageId}/replies | Reply in a DM message thread. |
| [**removeDMReaction**](DirectMessagesApi.md#removeDMReaction) | **DELETE** /v1/direct-messages/messages/{messageId}/reactions/{emoji} | Remove a DM message reaction. |
| [**searchDirectMessages**](DirectMessagesApi.md#searchDirectMessages) | **GET** /v1/direct-messages/search | Search across DM messages. |
| [**sendDirectMessage**](DirectMessagesApi.md#sendDirectMessage) | **POST** /v1/direct-messages/messages | Send a DM. |
| [**setDMDraft**](DirectMessagesApi.md#setDMDraft) | **PUT** /v1/direct-messages/{dmId}/draft | Save the unsent draft text for a DM. |
| [**unpinDMConversation**](DirectMessagesApi.md#unpinDMConversation) | **DELETE** /v1/direct-messages/{dmId}/pin | Unpin a DM conversation. |
| [**unpinDMMessage**](DirectMessagesApi.md#unpinDMMessage) | **DELETE** /v1/direct-messages/messages/{messageId}/pin | Unpin a DM message. |
| [**workspaceExecuteDMAction**](DirectMessagesApi.md#workspaceExecuteDMAction) | **POST** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/execute |  |
| [**workspaceGetDMUser**](DirectMessagesApi.md#workspaceGetDMUser) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/users/{id} |  |
| [**workspaceListDMActions**](DirectMessagesApi.md#workspaceListDMActions) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/actions |  |
| [**workspaceListDMConversations**](DirectMessagesApi.md#workspaceListDMConversations) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/conversations |  |
| [**workspaceListDMMessages**](DirectMessagesApi.md#workspaceListDMMessages) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/messages |  |
| [**workspaceListDMUsers**](DirectMessagesApi.md#workspaceListDMUsers) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/users |  |
| [**workspaceListDirectMessages**](DirectMessagesApi.md#workspaceListDirectMessages) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages |  |
| [**workspaceSendDirectMessage**](DirectMessagesApi.md#workspaceSendDirectMessage) | **POST** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/messages |  |


<a id="addDMReaction"></a>
# **addDMReaction**
> DMReactionResponse addDMReaction(messageId, dmReactionRequest)

React to a DM message.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val messageId : kotlin.String = messageId_example // kotlin.String | Chat-message id.
val dmReactionRequest : DMReactionRequest =  // DMReactionRequest | 
try {
    val result : DMReactionResponse = apiInstance.addDMReaction(messageId, dmReactionRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#addDMReaction")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#addDMReaction")
    e.printStackTrace()
}
```

### Parameters
| **messageId** | **kotlin.String**| Chat-message id. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dmReactionRequest** | [**DMReactionRequest**](DMReactionRequest.md)|  | |

### Return type

[**DMReactionResponse**](DMReactionResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="attachToDMMessage"></a>
# **attachToDMMessage**
> DMMessageEnvelope attachToDMMessage(messageId, dmAttachRequest)

Attach a file/image/etc. to an existing DM message.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val messageId : kotlin.String = messageId_example // kotlin.String | Chat-message id.
val dmAttachRequest : DMAttachRequest =  // DMAttachRequest | 
try {
    val result : DMMessageEnvelope = apiInstance.attachToDMMessage(messageId, dmAttachRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#attachToDMMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#attachToDMMessage")
    e.printStackTrace()
}
```

### Parameters
| **messageId** | **kotlin.String**| Chat-message id. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dmAttachRequest** | [**DMAttachRequest**](DMAttachRequest.md)|  | |

### Return type

[**DMMessageEnvelope**](DMMessageEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="executeDMAction"></a>
# **executeDMAction**
> ExecuteChatActionResponse executeDMAction(executeChatActionRequest)

Dispatch a DM action by id.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val executeChatActionRequest : ExecuteChatActionRequest =  // ExecuteChatActionRequest | 
try {
    val result : ExecuteChatActionResponse = apiInstance.executeDMAction(executeChatActionRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#executeDMAction")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#executeDMAction")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **executeChatActionRequest** | [**ExecuteChatActionRequest**](ExecuteChatActionRequest.md)|  | |

### Return type

[**ExecuteChatActionResponse**](ExecuteChatActionResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="forwardDMMessage"></a>
# **forwardDMMessage**
> DMMessageEnvelope forwardDMMessage(messageId, dmForwardRequest)

Forward a DM message to another DM or channel.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val messageId : kotlin.String = messageId_example // kotlin.String | Chat-message id.
val dmForwardRequest : DMForwardRequest =  // DMForwardRequest | 
try {
    val result : DMMessageEnvelope = apiInstance.forwardDMMessage(messageId, dmForwardRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#forwardDMMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#forwardDMMessage")
    e.printStackTrace()
}
```

### Parameters
| **messageId** | **kotlin.String**| Chat-message id. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dmForwardRequest** | [**DMForwardRequest**](DMForwardRequest.md)|  | |

### Return type

[**DMMessageEnvelope**](DMMessageEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="getDMUser"></a>
# **getDMUser**
> GetChatUserResponse getDMUser(id, accountId)

Fetch one chat user.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val id : kotlin.String = id_example // kotlin.String | Chat-user id (provider-scoped).
val accountId : kotlin.String = accountId_example // kotlin.String | 
try {
    val result : GetChatUserResponse = apiInstance.getDMUser(id, accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#getDMUser")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#getDMUser")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Chat-user id (provider-scoped). | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**|  | [optional] |

### Return type

[**GetChatUserResponse**](GetChatUserResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listDMActions"></a>
# **listDMActions**
> ChatActionsList listDMActions()

Discover the action catalog for DirectMessages.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
try {
    val result : ChatActionsList = apiInstance.listDMActions()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#listDMActions")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#listDMActions")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ChatActionsList**](ChatActionsList.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listDMPinnedMessages"></a>
# **listDMPinnedMessages**
> DMPinnedList listDMPinnedMessages(dmId, accountId)

List pinned messages in a DM conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val dmId : kotlin.String = dmId_example // kotlin.String | Direct-message conversation id.
val accountId : kotlin.String = accountId_example // kotlin.String | 
try {
    val result : DMPinnedList = apiInstance.listDMPinnedMessages(dmId, accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#listDMPinnedMessages")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#listDMPinnedMessages")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**| Direct-message conversation id. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**|  | [optional] |

### Return type

[**DMPinnedList**](DMPinnedList.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listDMThreadReplies"></a>
# **listDMThreadReplies**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listDMThreadReplies(dmId, messageId, accountId)

List replies in a DM message thread.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val dmId : kotlin.String = dmId_example // kotlin.String | Direct-message conversation id.
val messageId : kotlin.String = messageId_example // kotlin.String | Chat-message id.
val accountId : kotlin.String = accountId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listDMThreadReplies(dmId, messageId, accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#listDMThreadReplies")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#listDMThreadReplies")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**| Direct-message conversation id. | |
| **messageId** | **kotlin.String**| Chat-message id. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listDMUsers"></a>
# **listDMUsers**
> ListChatUsersResponse listDMUsers(accountIds, providers, xWorkspaceID, limit, cursor)

List chat users (DM contacts) across connected accounts.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val accountIds : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used. 
val providers : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`).
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val limit : kotlin.Int = 56 // kotlin.Int | 
val cursor : kotlin.String = cursor_example // kotlin.String | 
try {
    val result : ListChatUsersResponse = apiInstance.listDMUsers(accountIds, providers, xWorkspaceID, limit, cursor)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#listDMUsers")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#listDMUsers")
    e.printStackTrace()
}
```

### Parameters
| **accountIds** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] |
| **providers** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cursor** | **kotlin.String**|  | [optional] |

### Return type

[**ListChatUsersResponse**](ListChatUsersResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listDirectConversationsEnriched"></a>
# **listDirectConversationsEnriched**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listDirectConversationsEnriched(accountId, xWorkspaceID)

Enriched DM conversation list with unread + pin + draft state.

Native fast-path. Returns conversations augmented with the DM-feature state (unread counts, pinned/muted flags, saved drafts) the renderer&#39;s DM UI consumes. The shape is provider-specific and treated as opaque. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val accountId : kotlin.String = accountId_example // kotlin.String | 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listDirectConversationsEnriched(accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#listDirectConversationsEnriched")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#listDirectConversationsEnriched")
    e.printStackTrace()
}
```

### Parameters
| **accountId** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listDirectMessageConversations"></a>
# **listDirectMessageConversations**
> ListChannelsResponse listDirectMessageConversations(accountIds, providers, xWorkspaceID, limit, cursor, includeArchived)

List 1:1 and group DM conversations.

Returns DM-type conversations only (&#x60;type: im | mpim&#x60;). Channel-type conversations are surfaced via &#x60;/v1/channels&#x60;. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val accountIds : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used. 
val providers : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`).
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val limit : kotlin.Int = 56 // kotlin.Int | 
val cursor : kotlin.String = cursor_example // kotlin.String | 
val includeArchived : kotlin.Boolean = true // kotlin.Boolean | 
try {
    val result : ListChannelsResponse = apiInstance.listDirectMessageConversations(accountIds, providers, xWorkspaceID, limit, cursor, includeArchived)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#listDirectMessageConversations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#listDirectMessageConversations")
    e.printStackTrace()
}
```

### Parameters
| **accountIds** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] |
| **providers** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] |
| **cursor** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **includeArchived** | **kotlin.Boolean**|  | [optional] [default to false] |

### Return type

[**ListChannelsResponse**](ListChannelsResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listDirectMessages"></a>
# **listDirectMessages**
> ListMessagesResponse listDirectMessages(channel, accountId, accountIds, providers, xWorkspaceID, limit, cursor, oldestFirst)

List messages in a DM conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val channel : kotlin.String = channel_example // kotlin.String | DM conversation id.
val accountId : kotlin.String = accountId_example // kotlin.String | 
val accountIds : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used. 
val providers : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`).
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val limit : kotlin.Int = 56 // kotlin.Int | 
val cursor : kotlin.String = cursor_example // kotlin.String | 
val oldestFirst : kotlin.Boolean = true // kotlin.Boolean | 
try {
    val result : ListMessagesResponse = apiInstance.listDirectMessages(channel, accountId, accountIds, providers, xWorkspaceID, limit, cursor, oldestFirst)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#listDirectMessages")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#listDirectMessages")
    e.printStackTrace()
}
```

### Parameters
| **channel** | **kotlin.String**| DM conversation id. | |
| **accountId** | **kotlin.String**|  | [optional] |
| **accountIds** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] |
| **providers** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] |
| **cursor** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **oldestFirst** | **kotlin.Boolean**|  | [optional] |

### Return type

[**ListMessagesResponse**](ListMessagesResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="markDMRead"></a>
# **markDMRead**
> SuccessFlag markDMRead(dmId, dmMarkReadRequest)

Mark a DM message read.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val dmId : kotlin.String = dmId_example // kotlin.String | Direct-message conversation id.
val dmMarkReadRequest : DMMarkReadRequest =  // DMMarkReadRequest | 
try {
    val result : SuccessFlag = apiInstance.markDMRead(dmId, dmMarkReadRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#markDMRead")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#markDMRead")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**| Direct-message conversation id. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dmMarkReadRequest** | [**DMMarkReadRequest**](DMMarkReadRequest.md)|  | |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="muteDM"></a>
# **muteDM**
> DMMuteResponse muteDM(dmId, dmMuteRequest)

Mute a DM conversation (until a time, or forever).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val dmId : kotlin.String = dmId_example // kotlin.String | Direct-message conversation id.
val dmMuteRequest : DMMuteRequest =  // DMMuteRequest | 
try {
    val result : DMMuteResponse = apiInstance.muteDM(dmId, dmMuteRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#muteDM")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#muteDM")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**| Direct-message conversation id. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dmMuteRequest** | [**DMMuteRequest**](DMMuteRequest.md)|  | |

### Return type

[**DMMuteResponse**](DMMuteResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="pinDMConversation"></a>
# **pinDMConversation**
> SuccessFlag pinDMConversation(dmId, accountId)

Pin a DM conversation to the top of the sidebar.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val dmId : kotlin.String = dmId_example // kotlin.String | Direct-message conversation id.
val accountId : kotlin.String = accountId_example // kotlin.String | 
try {
    val result : SuccessFlag = apiInstance.pinDMConversation(dmId, accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#pinDMConversation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#pinDMConversation")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**| Direct-message conversation id. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**|  | [optional] |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="pinDMMessage"></a>
# **pinDMMessage**
> SuccessFlag pinDMMessage(messageId, channelMembershipRequest)

Pin a DM message.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val messageId : kotlin.String = messageId_example // kotlin.String | Chat-message id.
val channelMembershipRequest : ChannelMembershipRequest =  // ChannelMembershipRequest | 
try {
    val result : SuccessFlag = apiInstance.pinDMMessage(messageId, channelMembershipRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#pinDMMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#pinDMMessage")
    e.printStackTrace()
}
```

### Parameters
| **messageId** | **kotlin.String**| Chat-message id. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channelMembershipRequest** | [**ChannelMembershipRequest**](ChannelMembershipRequest.md)|  | [optional] |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="postDMThreadReply"></a>
# **postDMThreadReply**
> DMMessageEnvelope postDMThreadReply(dmId, messageId, dmThreadReplyRequest, accountId)

Reply in a DM message thread.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val dmId : kotlin.String = dmId_example // kotlin.String | Direct-message conversation id.
val messageId : kotlin.String = messageId_example // kotlin.String | Chat-message id.
val dmThreadReplyRequest : DMThreadReplyRequest =  // DMThreadReplyRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | 
try {
    val result : DMMessageEnvelope = apiInstance.postDMThreadReply(dmId, messageId, dmThreadReplyRequest, accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#postDMThreadReply")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#postDMThreadReply")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**| Direct-message conversation id. | |
| **messageId** | **kotlin.String**| Chat-message id. | |
| **dmThreadReplyRequest** | [**DMThreadReplyRequest**](DMThreadReplyRequest.md)|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**|  | [optional] |

### Return type

[**DMMessageEnvelope**](DMMessageEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="removeDMReaction"></a>
# **removeDMReaction**
> DMReactionResponse removeDMReaction(messageId, emoji, accountId)

Remove a DM message reaction.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val messageId : kotlin.String = messageId_example // kotlin.String | Chat-message id.
val emoji : kotlin.String = emoji_example // kotlin.String | Reaction emoji (e.g. `+1`, `eyes`, `pepper`).
val accountId : kotlin.String = accountId_example // kotlin.String | 
try {
    val result : DMReactionResponse = apiInstance.removeDMReaction(messageId, emoji, accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#removeDMReaction")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#removeDMReaction")
    e.printStackTrace()
}
```

### Parameters
| **messageId** | **kotlin.String**| Chat-message id. | |
| **emoji** | **kotlin.String**| Reaction emoji (e.g. &#x60;+1&#x60;, &#x60;eyes&#x60;, &#x60;pepper&#x60;). | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**|  | [optional] |

### Return type

[**DMReactionResponse**](DMReactionResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="searchDirectMessages"></a>
# **searchDirectMessages**
> DMSearchResults searchDirectMessages(q, limit, dmId, user, accountId)

Search across DM messages.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val q : kotlin.String = q_example // kotlin.String | Free-form query string.
val limit : kotlin.Int = 56 // kotlin.Int | 
val dmId : kotlin.String = dmId_example // kotlin.String | Restrict to one conversation.
val user : kotlin.String = user_example // kotlin.String | Restrict to messages from this user id.
val accountId : kotlin.String = accountId_example // kotlin.String | 
try {
    val result : DMSearchResults = apiInstance.searchDirectMessages(q, limit, dmId, user, accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#searchDirectMessages")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#searchDirectMessages")
    e.printStackTrace()
}
```

### Parameters
| **q** | **kotlin.String**| Free-form query string. | |
| **limit** | **kotlin.Int**|  | [optional] |
| **dmId** | **kotlin.String**| Restrict to one conversation. | [optional] |
| **user** | **kotlin.String**| Restrict to messages from this user id. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**|  | [optional] |

### Return type

[**DMSearchResults**](DMSearchResults.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="sendDirectMessage"></a>
# **sendDirectMessage**
> SendChatMessageResponse sendDirectMessage(sendChatMessageRequest)

Send a DM.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val sendChatMessageRequest : SendChatMessageRequest =  // SendChatMessageRequest | 
try {
    val result : SendChatMessageResponse = apiInstance.sendDirectMessage(sendChatMessageRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#sendDirectMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#sendDirectMessage")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sendChatMessageRequest** | [**SendChatMessageRequest**](SendChatMessageRequest.md)|  | |

### Return type

[**SendChatMessageResponse**](SendChatMessageResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="setDMDraft"></a>
# **setDMDraft**
> SuccessFlag setDMDraft(dmId, dmSetDraftRequest)

Save the unsent draft text for a DM.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val dmId : kotlin.String = dmId_example // kotlin.String | Direct-message conversation id.
val dmSetDraftRequest : DMSetDraftRequest =  // DMSetDraftRequest | 
try {
    val result : SuccessFlag = apiInstance.setDMDraft(dmId, dmSetDraftRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#setDMDraft")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#setDMDraft")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**| Direct-message conversation id. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dmSetDraftRequest** | [**DMSetDraftRequest**](DMSetDraftRequest.md)|  | |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="unpinDMConversation"></a>
# **unpinDMConversation**
> SuccessFlag unpinDMConversation(dmId, accountId)

Unpin a DM conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val dmId : kotlin.String = dmId_example // kotlin.String | Direct-message conversation id.
val accountId : kotlin.String = accountId_example // kotlin.String | 
try {
    val result : SuccessFlag = apiInstance.unpinDMConversation(dmId, accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#unpinDMConversation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#unpinDMConversation")
    e.printStackTrace()
}
```

### Parameters
| **dmId** | **kotlin.String**| Direct-message conversation id. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**|  | [optional] |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="unpinDMMessage"></a>
# **unpinDMMessage**
> SuccessFlag unpinDMMessage(messageId, accountId)

Unpin a DM message.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val messageId : kotlin.String = messageId_example // kotlin.String | Chat-message id.
val accountId : kotlin.String = accountId_example // kotlin.String | 
try {
    val result : SuccessFlag = apiInstance.unpinDMMessage(messageId, accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#unpinDMMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#unpinDMMessage")
    e.printStackTrace()
}
```

### Parameters
| **messageId** | **kotlin.String**| Chat-message id. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**|  | [optional] |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceExecuteDMAction"></a>
# **workspaceExecuteDMAction**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceExecuteDMAction(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceExecuteDMAction(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#workspaceExecuteDMAction")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#workspaceExecuteDMAction")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
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

<a id="workspaceGetDMUser"></a>
# **workspaceGetDMUser**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetDMUser(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetDMUser(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#workspaceGetDMUser")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#workspaceGetDMUser")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceListDMActions"></a>
# **workspaceListDMActions**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListDMActions(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListDMActions(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#workspaceListDMActions")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#workspaceListDMActions")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceListDMConversations"></a>
# **workspaceListDMConversations**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListDMConversations(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListDMConversations(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#workspaceListDMConversations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#workspaceListDMConversations")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceListDMMessages"></a>
# **workspaceListDMMessages**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListDMMessages(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListDMMessages(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#workspaceListDMMessages")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#workspaceListDMMessages")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceListDMUsers"></a>
# **workspaceListDMUsers**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListDMUsers(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListDMUsers(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#workspaceListDMUsers")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#workspaceListDMUsers")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceListDirectMessages"></a>
# **workspaceListDirectMessages**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListDirectMessages(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListDirectMessages(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#workspaceListDirectMessages")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#workspaceListDirectMessages")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceSendDirectMessage"></a>
# **workspaceSendDirectMessage**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceSendDirectMessage(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = DirectMessagesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceSendDirectMessage(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling DirectMessagesApi#workspaceSendDirectMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DirectMessagesApi#workspaceSendDirectMessage")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
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

