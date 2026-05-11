# AgentsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAgent**](AgentsApi.md#createAgent) | **POST** /v1/agents | Create a new agent configuration. |
| [**createAgentConversation**](AgentsApi.md#createAgentConversation) | **POST** /v1/agent/conversations | Create a new agent-platform conversation. |
| [**createAgentMessage**](AgentsApi.md#createAgentMessage) | **POST** /v1/agent/conversations/{id}/messages | Append a message to an agent conversation. |
| [**deleteAgent**](AgentsApi.md#deleteAgent) | **DELETE** /v1/agents/{id} | Delete an agent configuration. |
| [**executeAgentAction**](AgentsApi.md#executeAgentAction) | **POST** /v1/agent/actions/execute | Execute an action through the agent platform. |
| [**getAgent**](AgentsApi.md#getAgent) | **GET** /v1/agents/{id} | Fetch one agent configuration. |
| [**getAgentConversation**](AgentsApi.md#getAgentConversation) | **GET** /v1/agent/conversations/{id} | Fetch one agent conversation. |
| [**getAgentSessionContext**](AgentsApi.md#getAgentSessionContext) | **GET** /v1/agent/session-context | Identity bundle for the SessionStart hook (user + org + workspace + connected accounts) so the agent doesn&#39;t fish on its first turn.  |
| [**listAgentConversationMessages**](AgentsApi.md#listAgentConversationMessages) | **GET** /v1/agent/conversations/{id}/messages | List messages on an agent conversation. |
| [**listAgentConversations**](AgentsApi.md#listAgentConversations) | **GET** /v1/agent/conversations | List the caller&#39;s agent-platform conversations. Distinct from &#x60;/v1/conversations&#x60; (renderer-driven sidebar persistence).  |
| [**listAgents**](AgentsApi.md#listAgents) | **GET** /v1/agents | List the caller&#39;s agent configurations. |
| [**listPreconfiguredAgents**](AgentsApi.md#listPreconfiguredAgents) | **GET** /v1/agents/preconfigured | Curated featured agents (e.g. \&quot;Claude Code\&quot;, \&quot;Research Assistant\&quot;). Read-only — these are surfaced by the renderer&#39;s preconfigured-picker UI.  |
| [**updateAgent**](AgentsApi.md#updateAgent) | **PATCH** /v1/agents/{id} | Update an agent configuration. |


<a id="createAgent"></a>
# **createAgent**
> Agent createAgent(createAgentRequest)

Create a new agent configuration.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
val createAgentRequest : CreateAgentRequest =  // CreateAgentRequest | 
try {
    val result : Agent = apiInstance.createAgent(createAgentRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#createAgent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#createAgent")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createAgentRequest** | [**CreateAgentRequest**](CreateAgentRequest.md)|  | |

### Return type

[**Agent**](Agent.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createAgentConversation"></a>
# **createAgentConversation**
> AgentConversation createAgentConversation(createAgentConversationRequest)

Create a new agent-platform conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
val createAgentConversationRequest : CreateAgentConversationRequest =  // CreateAgentConversationRequest | 
try {
    val result : AgentConversation = apiInstance.createAgentConversation(createAgentConversationRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#createAgentConversation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#createAgentConversation")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createAgentConversationRequest** | [**CreateAgentConversationRequest**](CreateAgentConversationRequest.md)|  | [optional] |

### Return type

[**AgentConversation**](AgentConversation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createAgentMessage"></a>
# **createAgentMessage**
> AgentMessage createAgentMessage(id, createAgentMessageRequest)

Append a message to an agent conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
val id : kotlin.String = id_example // kotlin.String | 
val createAgentMessageRequest : CreateAgentMessageRequest =  // CreateAgentMessageRequest | 
try {
    val result : AgentMessage = apiInstance.createAgentMessage(id, createAgentMessageRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#createAgentMessage")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#createAgentMessage")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createAgentMessageRequest** | [**CreateAgentMessageRequest**](CreateAgentMessageRequest.md)|  | |

### Return type

[**AgentMessage**](AgentMessage.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteAgent"></a>
# **deleteAgent**
> deleteAgent(id)

Delete an agent configuration.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteAgent(id)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#deleteAgent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#deleteAgent")
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

<a id="executeAgentAction"></a>
# **executeAgentAction**
> ExecuteActionResponse executeAgentAction(executeActionRequest)

Execute an action through the agent platform.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
val executeActionRequest : ExecuteActionRequest =  // ExecuteActionRequest | 
try {
    val result : ExecuteActionResponse = apiInstance.executeAgentAction(executeActionRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#executeAgentAction")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#executeAgentAction")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **executeActionRequest** | [**ExecuteActionRequest**](ExecuteActionRequest.md)|  | |

### Return type

[**ExecuteActionResponse**](ExecuteActionResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="getAgent"></a>
# **getAgent**
> Agent getAgent(id)

Fetch one agent configuration.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : Agent = apiInstance.getAgent(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#getAgent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#getAgent")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**Agent**](Agent.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getAgentConversation"></a>
# **getAgentConversation**
> AgentConversation getAgentConversation(id)

Fetch one agent conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : AgentConversation = apiInstance.getAgentConversation(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#getAgentConversation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#getAgentConversation")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**AgentConversation**](AgentConversation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getAgentSessionContext"></a>
# **getAgentSessionContext**
> AgentSessionContext getAgentSessionContext()

Identity bundle for the SessionStart hook (user + org + workspace + connected accounts) so the agent doesn&#39;t fish on its first turn. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
try {
    val result : AgentSessionContext = apiInstance.getAgentSessionContext()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#getAgentSessionContext")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#getAgentSessionContext")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AgentSessionContext**](AgentSessionContext.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listAgentConversationMessages"></a>
# **listAgentConversationMessages**
> AgentMessageListResponse listAgentConversationMessages(id)

List messages on an agent conversation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : AgentMessageListResponse = apiInstance.listAgentConversationMessages(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#listAgentConversationMessages")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#listAgentConversationMessages")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**AgentMessageListResponse**](AgentMessageListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listAgentConversations"></a>
# **listAgentConversations**
> AgentConversationListResponse listAgentConversations()

List the caller&#39;s agent-platform conversations. Distinct from &#x60;/v1/conversations&#x60; (renderer-driven sidebar persistence). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
try {
    val result : AgentConversationListResponse = apiInstance.listAgentConversations()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#listAgentConversations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#listAgentConversations")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AgentConversationListResponse**](AgentConversationListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listAgents"></a>
# **listAgents**
> AgentListResponse listAgents()

List the caller&#39;s agent configurations.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
try {
    val result : AgentListResponse = apiInstance.listAgents()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#listAgents")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#listAgents")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AgentListResponse**](AgentListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listPreconfiguredAgents"></a>
# **listPreconfiguredAgents**
> kotlin.collections.List&lt;PreconfiguredAgent&gt; listPreconfiguredAgents()

Curated featured agents (e.g. \&quot;Claude Code\&quot;, \&quot;Research Assistant\&quot;). Read-only — these are surfaced by the renderer&#39;s preconfigured-picker UI. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
try {
    val result : kotlin.collections.List<PreconfiguredAgent> = apiInstance.listPreconfiguredAgents()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#listPreconfiguredAgents")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#listPreconfiguredAgents")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**kotlin.collections.List&lt;PreconfiguredAgent&gt;**](PreconfiguredAgent.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateAgent"></a>
# **updateAgent**
> Agent updateAgent(id, updateAgentRequest)

Update an agent configuration.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = AgentsApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateAgentRequest : UpdateAgentRequest =  // UpdateAgentRequest | 
try {
    val result : Agent = apiInstance.updateAgent(id, updateAgentRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AgentsApi#updateAgent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AgentsApi#updateAgent")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateAgentRequest** | [**UpdateAgentRequest**](UpdateAgentRequest.md)|  | |

### Return type

[**Agent**](Agent.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

