# WorkspacesApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**acceptWorkspaceInvitation**](WorkspacesApi.md#acceptWorkspaceInvitation) | **POST** /v1/invitations/{token}/accept | Accept a workspace invitation by token. The signed-in user&#39;s email must match the invitation. Organization-token accept lives at &#x60;POST /v1/organizations/{org}/accept-invitation&#x60;.  |
| [**addWorkspaceMember**](WorkspacesApi.md#addWorkspaceMember) | **POST** /v1/workspaces/{workspaceId}/members | Add a member directly (skips invitation flow). |
| [**createWorkspace**](WorkspacesApi.md#createWorkspace) | **POST** /v1/workspaces | Create a workspace. Requires &#x60;organizationId&#x60; in the body — bare \&quot;personal\&quot; workspaces aren&#39;t supported on the public API.  |
| [**createWorkspaceInvitation**](WorkspacesApi.md#createWorkspaceInvitation) | **POST** /v1/workspaces/{workspaceId}/invitations | Invite a user to a workspace. |
| [**getPublicInvitation**](WorkspacesApi.md#getPublicInvitation) | **GET** /invitations/{token} | Fetch invitation details by token (unauthenticated). Used by the renderer to show invitation context before the user signs in.  |
| [**getWorkspace**](WorkspacesApi.md#getWorkspace) | **GET** /v1/workspaces/{workspaceId} | Fetch a single workspace by id. |
| [**listMyWorkspaces**](WorkspacesApi.md#listMyWorkspaces) | **GET** /v1/workspaces | List the caller&#39;s workspaces (across organizations). |
| [**listWorkspaceInvitations**](WorkspacesApi.md#listWorkspaceInvitations) | **GET** /v1/workspaces/{workspaceId}/invitations | List pending workspace invitations. |
| [**listWorkspaceMembers**](WorkspacesApi.md#listWorkspaceMembers) | **GET** /v1/workspaces/{workspaceId}/members | List members of a workspace. |
| [**removeWorkspaceMember**](WorkspacesApi.md#removeWorkspaceMember) | **DELETE** /v1/workspaces/{workspaceId}/members/{memberId} | Remove a member from the workspace. |
| [**revokeWorkspaceInvitation**](WorkspacesApi.md#revokeWorkspaceInvitation) | **DELETE** /v1/workspaces/{workspaceId}/invitations/{invitationId} | Revoke a pending workspace invitation. |
| [**updateWorkspace**](WorkspacesApi.md#updateWorkspace) | **PATCH** /v1/workspaces/{workspaceId} | Update workspace metadata. |
| [**updateWorkspaceMember**](WorkspacesApi.md#updateWorkspaceMember) | **PATCH** /v1/workspaces/{workspaceId}/members/{memberId} | Update a member&#39;s role. |


<a id="acceptWorkspaceInvitation"></a>
# **acceptWorkspaceInvitation**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; acceptWorkspaceInvitation(token)

Accept a workspace invitation by token. The signed-in user&#39;s email must match the invitation. Organization-token accept lives at &#x60;POST /v1/organizations/{org}/accept-invitation&#x60;. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
val token : kotlin.String = token_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.acceptWorkspaceInvitation(token)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#acceptWorkspaceInvitation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#acceptWorkspaceInvitation")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **token** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="addWorkspaceMember"></a>
# **addWorkspaceMember**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; addWorkspaceMember(workspaceId, addWorkspaceMemberRequest)

Add a member directly (skips invitation flow).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val addWorkspaceMemberRequest : AddWorkspaceMemberRequest =  // AddWorkspaceMemberRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.addWorkspaceMember(workspaceId, addWorkspaceMemberRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#addWorkspaceMember")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#addWorkspaceMember")
    e.printStackTrace()
}
```

### Parameters
| **workspaceId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **addWorkspaceMemberRequest** | [**AddWorkspaceMemberRequest**](AddWorkspaceMemberRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createWorkspace"></a>
# **createWorkspace**
> WorkspaceEnvelope createWorkspace(createWorkspaceRequest)

Create a workspace. Requires &#x60;organizationId&#x60; in the body — bare \&quot;personal\&quot; workspaces aren&#39;t supported on the public API. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
val createWorkspaceRequest : CreateWorkspaceRequest =  // CreateWorkspaceRequest | 
try {
    val result : WorkspaceEnvelope = apiInstance.createWorkspace(createWorkspaceRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#createWorkspace")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#createWorkspace")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createWorkspaceRequest** | [**CreateWorkspaceRequest**](CreateWorkspaceRequest.md)|  | |

### Return type

[**WorkspaceEnvelope**](WorkspaceEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createWorkspaceInvitation"></a>
# **createWorkspaceInvitation**
> WorkspaceInvitation createWorkspaceInvitation(workspaceId, createWorkspaceInvitationRequest)

Invite a user to a workspace.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val createWorkspaceInvitationRequest : CreateWorkspaceInvitationRequest =  // CreateWorkspaceInvitationRequest | 
try {
    val result : WorkspaceInvitation = apiInstance.createWorkspaceInvitation(workspaceId, createWorkspaceInvitationRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#createWorkspaceInvitation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#createWorkspaceInvitation")
    e.printStackTrace()
}
```

### Parameters
| **workspaceId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createWorkspaceInvitationRequest** | [**CreateWorkspaceInvitationRequest**](CreateWorkspaceInvitationRequest.md)|  | |

### Return type

[**WorkspaceInvitation**](WorkspaceInvitation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="getPublicInvitation"></a>
# **getPublicInvitation**
> PublicInvitationPayload getPublicInvitation(token)

Fetch invitation details by token (unauthenticated). Used by the renderer to show invitation context before the user signs in. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
val token : kotlin.String = token_example // kotlin.String | 
try {
    val result : PublicInvitationPayload = apiInstance.getPublicInvitation(token)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#getPublicInvitation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#getPublicInvitation")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **token** | **kotlin.String**|  | |

### Return type

[**PublicInvitationPayload**](PublicInvitationPayload.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getWorkspace"></a>
# **getWorkspace**
> WorkspaceEnvelope getWorkspace(workspaceId)

Fetch a single workspace by id.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
try {
    val result : WorkspaceEnvelope = apiInstance.getWorkspace(workspaceId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#getWorkspace")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#getWorkspace")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspaceId** | **kotlin.String**|  | |

### Return type

[**WorkspaceEnvelope**](WorkspaceEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listMyWorkspaces"></a>
# **listMyWorkspaces**
> WorkspaceListResponse listMyWorkspaces()

List the caller&#39;s workspaces (across organizations).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
try {
    val result : WorkspaceListResponse = apiInstance.listMyWorkspaces()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#listMyWorkspaces")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#listMyWorkspaces")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**WorkspaceListResponse**](WorkspaceListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listWorkspaceInvitations"></a>
# **listWorkspaceInvitations**
> WorkspaceInvitationListResponse listWorkspaceInvitations(workspaceId)

List pending workspace invitations.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
try {
    val result : WorkspaceInvitationListResponse = apiInstance.listWorkspaceInvitations(workspaceId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#listWorkspaceInvitations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#listWorkspaceInvitations")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspaceId** | **kotlin.String**|  | |

### Return type

[**WorkspaceInvitationListResponse**](WorkspaceInvitationListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listWorkspaceMembers"></a>
# **listWorkspaceMembers**
> WorkspaceMemberListResponse listWorkspaceMembers(workspaceId)

List members of a workspace.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
try {
    val result : WorkspaceMemberListResponse = apiInstance.listWorkspaceMembers(workspaceId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#listWorkspaceMembers")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#listWorkspaceMembers")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspaceId** | **kotlin.String**|  | |

### Return type

[**WorkspaceMemberListResponse**](WorkspaceMemberListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="removeWorkspaceMember"></a>
# **removeWorkspaceMember**
> removeWorkspaceMember(workspaceId, memberId)

Remove a member from the workspace.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val memberId : kotlin.String = memberId_example // kotlin.String | 
try {
    apiInstance.removeWorkspaceMember(workspaceId, memberId)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#removeWorkspaceMember")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#removeWorkspaceMember")
    e.printStackTrace()
}
```

### Parameters
| **workspaceId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **memberId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="revokeWorkspaceInvitation"></a>
# **revokeWorkspaceInvitation**
> revokeWorkspaceInvitation(workspaceId, invitationId)

Revoke a pending workspace invitation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val invitationId : kotlin.String = invitationId_example // kotlin.String | 
try {
    apiInstance.revokeWorkspaceInvitation(workspaceId, invitationId)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#revokeWorkspaceInvitation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#revokeWorkspaceInvitation")
    e.printStackTrace()
}
```

### Parameters
| **workspaceId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invitationId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateWorkspace"></a>
# **updateWorkspace**
> WorkspaceEnvelope updateWorkspace(workspaceId, updateWorkspaceRequest)

Update workspace metadata.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val updateWorkspaceRequest : UpdateWorkspaceRequest =  // UpdateWorkspaceRequest | 
try {
    val result : WorkspaceEnvelope = apiInstance.updateWorkspace(workspaceId, updateWorkspaceRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#updateWorkspace")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#updateWorkspace")
    e.printStackTrace()
}
```

### Parameters
| **workspaceId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateWorkspaceRequest** | [**UpdateWorkspaceRequest**](UpdateWorkspaceRequest.md)|  | |

### Return type

[**WorkspaceEnvelope**](WorkspaceEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateWorkspaceMember"></a>
# **updateWorkspaceMember**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateWorkspaceMember(workspaceId, memberId, updateWorkspaceMemberRequest)

Update a member&#39;s role.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = WorkspacesApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val memberId : kotlin.String = memberId_example // kotlin.String | 
val updateWorkspaceMemberRequest : UpdateWorkspaceMemberRequest =  // UpdateWorkspaceMemberRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateWorkspaceMember(workspaceId, memberId, updateWorkspaceMemberRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkspacesApi#updateWorkspaceMember")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkspacesApi#updateWorkspaceMember")
    e.printStackTrace()
}
```

### Parameters
| **workspaceId** | **kotlin.String**|  | |
| **memberId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateWorkspaceMemberRequest** | [**UpdateWorkspaceMemberRequest**](UpdateWorkspaceMemberRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

