# ChannelsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createChannel**](ChannelsApi.md#createChannel) | **POST** /v1/channels | Create a channel. |
| [**executeChannelAction**](ChannelsApi.md#executeChannelAction) | **POST** /v1/channels/execute | Dispatch a channel action by id. |
| [**joinChannel**](ChannelsApi.md#joinChannel) | **POST** /v1/channels/{id}/join | Join a channel. |
| [**leaveChannel**](ChannelsApi.md#leaveChannel) | **POST** /v1/channels/{id}/leave | Leave a channel. |
| [**listChannelActions**](ChannelsApi.md#listChannelActions) | **GET** /v1/channels/actions | Discover the action catalog for the Channels platform. |
| [**listChannelMessages**](ChannelsApi.md#listChannelMessages) | **GET** /v1/channels/messages | List messages in a channel. |
| [**listChannels**](ChannelsApi.md#listChannels) | **GET** /v1/channels | List group channels across connected chat providers. |
| [**sendChannelMessage**](ChannelsApi.md#sendChannelMessage) | **POST** /v1/channels/messages | Send a message to a channel. |
| [**workspaceCreateChannel**](ChannelsApi.md#workspaceCreateChannel) | **POST** /v1/organizations/{org}/workspaces/{workspace}/channels |  |
| [**workspaceExecuteChannelAction**](ChannelsApi.md#workspaceExecuteChannelAction) | **POST** /v1/organizations/{org}/workspaces/{workspace}/channels/execute |  |
| [**workspaceJoinChannel**](ChannelsApi.md#workspaceJoinChannel) | **POST** /v1/organizations/{org}/workspaces/{workspace}/channels/{id}/join |  |
| [**workspaceLeaveChannel**](ChannelsApi.md#workspaceLeaveChannel) | **POST** /v1/organizations/{org}/workspaces/{workspace}/channels/{id}/leave |  |
| [**workspaceListChannelActions**](ChannelsApi.md#workspaceListChannelActions) | **GET** /v1/organizations/{org}/workspaces/{workspace}/channels/actions |  |
| [**workspaceListChannelMessages**](ChannelsApi.md#workspaceListChannelMessages) | **GET** /v1/organizations/{org}/workspaces/{workspace}/channels/messages |  |
| [**workspaceListChannels**](ChannelsApi.md#workspaceListChannels) | **GET** /v1/organizations/{org}/workspaces/{workspace}/channels |  |
| [**workspaceSendChannelMessage**](ChannelsApi.md#workspaceSendChannelMessage) | **POST** /v1/organizations/{org}/workspaces/{workspace}/channels/messages |  |


<a id="createChannel"></a>
# **createChannel**
> CreateChannelResponse createChannel(createChannelRequest)

Create a channel.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val createChannelRequest : CreateChannelRequest =  // CreateChannelRequest | 
try {
    val result : CreateChannelResponse = apiInstance.createChannel(createChannelRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#createChannel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#createChannel")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createChannelRequest** | [**CreateChannelRequest**](CreateChannelRequest.md)|  | |

### Return type

[**CreateChannelResponse**](CreateChannelResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="executeChannelAction"></a>
# **executeChannelAction**
> ExecuteChatActionResponse executeChannelAction(executeChatActionRequest)

Dispatch a channel action by id.

Generic action-execution endpoint. &#x60;params&#x60; shape varies per &#x60;action_id&#x60;; consult &#x60;GET /v1/channels/actions&#x60; for the per-id contract. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val executeChatActionRequest : ExecuteChatActionRequest =  // ExecuteChatActionRequest | 
try {
    val result : ExecuteChatActionResponse = apiInstance.executeChannelAction(executeChatActionRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#executeChannelAction")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#executeChannelAction")
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

<a id="joinChannel"></a>
# **joinChannel**
> SuccessFlag joinChannel(id, channelMembershipRequest)

Join a channel.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val id : kotlin.String = id_example // kotlin.String | Channel id (provider-scoped).
val channelMembershipRequest : ChannelMembershipRequest =  // ChannelMembershipRequest | 
try {
    val result : SuccessFlag = apiInstance.joinChannel(id, channelMembershipRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#joinChannel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#joinChannel")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Channel id (provider-scoped). | |
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

<a id="leaveChannel"></a>
# **leaveChannel**
> SuccessFlag leaveChannel(id, channelMembershipRequest)

Leave a channel.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val id : kotlin.String = id_example // kotlin.String | Channel id (provider-scoped).
val channelMembershipRequest : ChannelMembershipRequest =  // ChannelMembershipRequest | 
try {
    val result : SuccessFlag = apiInstance.leaveChannel(id, channelMembershipRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#leaveChannel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#leaveChannel")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Channel id (provider-scoped). | |
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

<a id="listChannelActions"></a>
# **listChannelActions**
> ChatActionsList listChannelActions()

Discover the action catalog for the Channels platform.

Returns the action descriptors the agent layer dispatches via &#x60;POST /v1/channels/execute&#x60;. Same pattern as the DirectMessages action surface. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
try {
    val result : ChatActionsList = apiInstance.listChannelActions()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#listChannelActions")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#listChannelActions")
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

<a id="listChannelMessages"></a>
# **listChannelMessages**
> ListMessagesResponse listChannelMessages(channel, accountId, accountIds, providers, xWorkspaceID, limit, cursor, oldestFirst)

List messages in a channel.

Channel ids are provider-scoped; pass &#x60;?accountId&#x3D;&#x60; (preferred) or &#x60;?accountIds&#x3D;&#x60; to disambiguate when the same id exists on multiple connected accounts (rare). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val channel : kotlin.String = channel_example // kotlin.String | Channel id.
val accountId : kotlin.String = accountId_example // kotlin.String | 
val accountIds : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used. 
val providers : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`).
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val limit : kotlin.Int = 56 // kotlin.Int | 
val cursor : kotlin.String = cursor_example // kotlin.String | 
val oldestFirst : kotlin.Boolean = true // kotlin.Boolean | 
try {
    val result : ListMessagesResponse = apiInstance.listChannelMessages(channel, accountId, accountIds, providers, xWorkspaceID, limit, cursor, oldestFirst)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#listChannelMessages")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#listChannelMessages")
    e.printStackTrace()
}
```

### Parameters
| **channel** | **kotlin.String**| Channel id. | |
| **accountId** | **kotlin.String**|  | [optional] |
| **accountIds** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] |
| **providers** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] |
| **cursor** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **oldestFirst** | **kotlin.Boolean**|  | [optional] [default to false] |

### Return type

[**ListMessagesResponse**](ListMessagesResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listChannels"></a>
# **listChannels**
> ListChannelsResponse listChannels(accountIds, providers, xWorkspaceID, limit, cursor, includeArchived, types)

List group channels across connected chat providers.

Fan-out list. The Channels surface filters to channel-type conversations only (&#x60;type: channel | private&#x60;); for direct messages use &#x60;/v1/direct-messages&#x60;. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val accountIds : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used. 
val providers : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`).
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val limit : kotlin.Int = 56 // kotlin.Int | 
val cursor : kotlin.String = cursor_example // kotlin.String | Provider-specific pagination cursor.
val includeArchived : kotlin.Boolean = true // kotlin.Boolean | 
val types : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable filter on `Channel.type`. Defaults applied by the platform exclude DMs; passing this overrides. 
try {
    val result : ListChannelsResponse = apiInstance.listChannels(accountIds, providers, xWorkspaceID, limit, cursor, includeArchived, types)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#listChannels")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#listChannels")
    e.printStackTrace()
}
```

### Parameters
| **accountIds** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] |
| **providers** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] |
| **cursor** | **kotlin.String**| Provider-specific pagination cursor. | [optional] |
| **includeArchived** | **kotlin.Boolean**|  | [optional] [default to false] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **types** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable filter on &#x60;Channel.type&#x60;. Defaults applied by the platform exclude DMs; passing this overrides.  | [optional] |

### Return type

[**ListChannelsResponse**](ListChannelsResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="sendChannelMessage"></a>
# **sendChannelMessage**
> SendChatMessageResponse sendChannelMessage(sendChatMessageRequest)

Send a message to a channel.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val sendChatMessageRequest : SendChatMessageRequest =  // SendChatMessageRequest | 
try {
    val result : SendChatMessageResponse = apiInstance.sendChannelMessage(sendChatMessageRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#sendChannelMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#sendChannelMessage")
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

<a id="workspaceCreateChannel"></a>
# **workspaceCreateChannel**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateChannel(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateChannel(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#workspaceCreateChannel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#workspaceCreateChannel")
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

<a id="workspaceExecuteChannelAction"></a>
# **workspaceExecuteChannelAction**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceExecuteChannelAction(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceExecuteChannelAction(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#workspaceExecuteChannelAction")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#workspaceExecuteChannelAction")
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

<a id="workspaceJoinChannel"></a>
# **workspaceJoinChannel**
> workspaceJoinChannel(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    apiInstance.workspaceJoinChannel(org, workspace, id, requestBody)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#workspaceJoinChannel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#workspaceJoinChannel")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **id** | **kotlin.String**|  | |
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

<a id="workspaceLeaveChannel"></a>
# **workspaceLeaveChannel**
> workspaceLeaveChannel(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    apiInstance.workspaceLeaveChannel(org, workspace, id, requestBody)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#workspaceLeaveChannel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#workspaceLeaveChannel")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **id** | **kotlin.String**|  | |
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

<a id="workspaceListChannelActions"></a>
# **workspaceListChannelActions**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListChannelActions(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListChannelActions(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#workspaceListChannelActions")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#workspaceListChannelActions")
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

<a id="workspaceListChannelMessages"></a>
# **workspaceListChannelMessages**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListChannelMessages(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListChannelMessages(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#workspaceListChannelMessages")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#workspaceListChannelMessages")
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

<a id="workspaceListChannels"></a>
# **workspaceListChannels**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListChannels(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListChannels(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#workspaceListChannels")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#workspaceListChannels")
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

<a id="workspaceSendChannelMessage"></a>
# **workspaceSendChannelMessage**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceSendChannelMessage(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ChannelsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceSendChannelMessage(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ChannelsApi#workspaceSendChannelMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ChannelsApi#workspaceSendChannelMessage")
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

