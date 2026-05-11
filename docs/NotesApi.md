# NotesApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createBlock**](NotesApi.md#createBlock) | **POST** /v1/notes/{id}/blocks | Insert a block in a note. |
| [**createNote**](NotesApi.md#createNote) | **POST** /v1/notes | Create a note. |
| [**createNoteComment**](NotesApi.md#createNoteComment) | **POST** /v1/notes/{id}/comments | Create a comment or reply. |
| [**deleteBlock**](NotesApi.md#deleteBlock) | **DELETE** /v1/notes/blocks/{id} | Delete a block. |
| [**deleteNote**](NotesApi.md#deleteNote) | **DELETE** /v1/notes/{id} | Delete a note. |
| [**deleteNoteComment**](NotesApi.md#deleteNoteComment) | **DELETE** /v1/notes/{id}/comments/{commentId} | Soft-delete (native) or hard-delete (provider) a comment. |
| [**disableNoteShare**](NotesApi.md#disableNoteShare) | **DELETE** /v1/notes/{id}/share | Disable public sharing. |
| [**enableNoteShare**](NotesApi.md#enableNoteShare) | **POST** /v1/notes/{id}/share | Enable (or update password on) public sharing. |
| [**getBlock**](NotesApi.md#getBlock) | **GET** /v1/notes/blocks/{id} | Fetch one block. |
| [**getNote**](NotesApi.md#getNote) | **GET** /v1/notes/{id} | Fetch one note. |
| [**getNoteComment**](NotesApi.md#getNoteComment) | **GET** /v1/notes/{id}/comments/{commentId} | Fetch one comment. |
| [**getNoteShareSettings**](NotesApi.md#getNoteShareSettings) | **GET** /v1/notes/{id}/share | Fetch share settings for a note. |
| [**getPublicNote**](NotesApi.md#getPublicNote) | **GET** /public/notes/{token} | Fetch a publicly shared note. |
| [**listBlocks**](NotesApi.md#listBlocks) | **GET** /v1/notes/{id}/blocks | List blocks under a note. |
| [**listNoteComments**](NotesApi.md#listNoteComments) | **GET** /v1/notes/{id}/comments | List comments on a note. |
| [**listNotes**](NotesApi.md#listNotes) | **GET** /v1/notes | List notes across connected accounts. |
| [**moveBlock**](NotesApi.md#moveBlock) | **POST** /v1/notes/blocks/{id}/move | Reparent or reorder a block. |
| [**rotateNoteShareToken**](NotesApi.md#rotateNoteShareToken) | **POST** /v1/notes/{id}/share/rotate | Rotate the share token, invalidating any outstanding URLs. |
| [**updateBlock**](NotesApi.md#updateBlock) | **PATCH** /v1/notes/blocks/{id} | Update a block (partial). |
| [**updateNote**](NotesApi.md#updateNote) | **PATCH** /v1/notes/{id} | Update a note (partial). |
| [**updateNoteComment**](NotesApi.md#updateNoteComment) | **PATCH** /v1/notes/{id}/comments/{commentId} | Edit a comment. |
| [**workspaceCreateNote**](NotesApi.md#workspaceCreateNote) | **POST** /v1/organizations/{org}/workspaces/{workspace}/notes |  |
| [**workspaceCreateNoteBlock**](NotesApi.md#workspaceCreateNoteBlock) | **POST** /v1/organizations/{org}/workspaces/{workspace}/notes/{id}/blocks |  |
| [**workspaceDeleteNote**](NotesApi.md#workspaceDeleteNote) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/notes/{id} |  |
| [**workspaceDeleteNoteBlock**](NotesApi.md#workspaceDeleteNoteBlock) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/notes/blocks/{id} |  |
| [**workspaceGetNote**](NotesApi.md#workspaceGetNote) | **GET** /v1/organizations/{org}/workspaces/{workspace}/notes/{id} |  |
| [**workspaceGetNoteBlock**](NotesApi.md#workspaceGetNoteBlock) | **GET** /v1/organizations/{org}/workspaces/{workspace}/notes/blocks/{id} |  |
| [**workspaceListNoteBlocks**](NotesApi.md#workspaceListNoteBlocks) | **GET** /v1/organizations/{org}/workspaces/{workspace}/notes/{id}/blocks |  |
| [**workspaceListNotes**](NotesApi.md#workspaceListNotes) | **GET** /v1/organizations/{org}/workspaces/{workspace}/notes |  |
| [**workspaceMoveNoteBlock**](NotesApi.md#workspaceMoveNoteBlock) | **POST** /v1/organizations/{org}/workspaces/{workspace}/notes/blocks/{id}/move |  |
| [**workspaceUpdateNote**](NotesApi.md#workspaceUpdateNote) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/notes/{id} |  |
| [**workspaceUpdateNoteBlock**](NotesApi.md#workspaceUpdateNoteBlock) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/notes/blocks/{id} |  |


<a id="createBlock"></a>
# **createBlock**
> Block createBlock(id, createBlockRequest, accountId, xWorkspaceID)

Insert a block in a note.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val createBlockRequest : CreateBlockRequest =  // CreateBlockRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Block = apiInstance.createBlock(id, createBlockRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#createBlock")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#createBlock")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **createBlockRequest** | [**CreateBlockRequest**](CreateBlockRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Block**](Block.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createNote"></a>
# **createNote**
> Note createNote(createNoteRequest, accountId, provider, xWorkspaceID)

Create a note.

Creates a new note under the target account. The target is resolved in this order: &#x60;accountId&#x60; field on the body → &#x60;?accountId&#x3D;&#x60; query → &#x60;provider&#x60; field on the body → &#x60;?provider&#x3D;&#x60; query → the caller&#39;s single connected account (errors with &#x60;ambiguous_account&#x60; if more than one is connected and no selector is supplied). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val createNoteRequest : CreateNoteRequest =  // CreateNoteRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Note = apiInstance.createNote(createNoteRequest, accountId, provider, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#createNote")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#createNote")
    e.printStackTrace()
}
```

### Parameters
| **createNoteRequest** | [**CreateNoteRequest**](CreateNoteRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **provider** | **kotlin.String**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Note**](Note.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createNoteComment"></a>
# **createNoteComment**
> CommentMutationResponse createNoteComment(id, createCommentRequest, accountId, xWorkspaceID)

Create a comment or reply.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val createCommentRequest : CreateCommentRequest =  // CreateCommentRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : CommentMutationResponse = apiInstance.createNoteComment(id, createCommentRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#createNoteComment")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#createNoteComment")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **createCommentRequest** | [**CreateCommentRequest**](CreateCommentRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**CommentMutationResponse**](CommentMutationResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteBlock"></a>
# **deleteBlock**
> SuccessFlag deleteBlock(id, accountId, xWorkspaceID)

Delete a block.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Block id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.deleteBlock(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#deleteBlock")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#deleteBlock")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Block id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="deleteNote"></a>
# **deleteNote**
> SuccessFlag deleteNote(id, accountId, xWorkspaceID)

Delete a note.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.deleteNote(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#deleteNote")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#deleteNote")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="deleteNoteComment"></a>
# **deleteNoteComment**
> SuccessFlag deleteNoteComment(id, commentId, accountId, xWorkspaceID)

Soft-delete (native) or hard-delete (provider) a comment.

Allowed for the comment author and for the note owner. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val commentId : kotlin.String = commentId_example // kotlin.String | Comment id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.deleteNoteComment(id, commentId, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#deleteNoteComment")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#deleteNoteComment")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **commentId** | **kotlin.String**| Comment id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="disableNoteShare"></a>
# **disableNoteShare**
> disableNoteShare(id, accountId, xWorkspaceID)

Disable public sharing.

Owner-only. Subsequent public viewer requests 404.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    apiInstance.disableNoteShare(id, accountId, xWorkspaceID)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#disableNoteShare")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#disableNoteShare")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="enableNoteShare"></a>
# **enableNoteShare**
> ShareSettings enableNoteShare(id, accountId, xWorkspaceID, enableShareRequest)

Enable (or update password on) public sharing.

Owner-only. Calling with an empty body or &#x60;setPassword: false&#x60; flips the note public without changing the password. With &#x60;setPassword: true&#x60;, applies &#x60;password&#x60; (empty string clears). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val enableShareRequest : EnableShareRequest =  // EnableShareRequest | 
try {
    val result : ShareSettings = apiInstance.enableNoteShare(id, accountId, xWorkspaceID, enableShareRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#enableNoteShare")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#enableNoteShare")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **enableShareRequest** | [**EnableShareRequest**](EnableShareRequest.md)|  | [optional] |

### Return type

[**ShareSettings**](ShareSettings.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="getBlock"></a>
# **getBlock**
> Block getBlock(id, accountId, xWorkspaceID)

Fetch one block.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Block id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Block = apiInstance.getBlock(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#getBlock")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#getBlock")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Block id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Block**](Block.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getNote"></a>
# **getNote**
> Note getNote(id, accountId, xWorkspaceID)

Fetch one note.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Note = apiInstance.getNote(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#getNote")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#getNote")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Note**](Note.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getNoteComment"></a>
# **getNoteComment**
> CommentResponse getNoteComment(id, commentId, accountId, xWorkspaceID)

Fetch one comment.

Useful for permalink hydration when the renderer deep-links into a reply thread. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val commentId : kotlin.String = commentId_example // kotlin.String | Comment id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : CommentResponse = apiInstance.getNoteComment(id, commentId, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#getNoteComment")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#getNoteComment")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **commentId** | **kotlin.String**| Comment id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**CommentResponse**](CommentResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getNoteShareSettings"></a>
# **getNoteShareSettings**
> ShareSettings getNoteShareSettings(id, accountId, xWorkspaceID)

Fetch share settings for a note.

Owner-only. Returns the current public-share configuration, including the share token and computed public viewer URL when the note is currently public. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : ShareSettings = apiInstance.getNoteShareSettings(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#getNoteShareSettings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#getNoteShareSettings")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**ShareSettings**](ShareSettings.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getPublicNote"></a>
# **getPublicNote**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getPublicNote(token, password)

Fetch a publicly shared note.

Unauthenticated. The share token is the credential. For password-protected notes the password is supplied via the &#x60;?password&#x3D;&#x60; query param; the response distinguishes \&quot;no password supplied\&quot; from \&quot;wrong password\&quot; so the viewer can render the right prompt.  Unknown tokens and disabled-share notes both return &#x60;404&#x60; to prevent token enumeration. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val token : kotlin.String = token_example // kotlin.String | Opaque public-share token.
val password : kotlin.String = password_example // kotlin.String | Optional viewer password.
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getPublicNote(token, password)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#getPublicNote")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#getPublicNote")
    e.printStackTrace()
}
```

### Parameters
| **token** | **kotlin.String**| Opaque public-share token. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **password** | **kotlin.String**| Optional viewer password. | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listBlocks"></a>
# **listBlocks**
> BlockListResponse listBlocks(id, accountId, xWorkspaceID, parentId, limit, offset)

List blocks under a note.

Returns the block tree for a note, paginated. Block listing always targets a single account (the one that owns the note) so it does not fan out — the response is a plain &#x60;{ blocks, total }&#x60;. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val parentId : kotlin.String = parentId_example // kotlin.String | Filter to children of this block id. Omit to list root-level blocks. 
val limit : kotlin.Int = 56 // kotlin.Int | 
val offset : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : BlockListResponse = apiInstance.listBlocks(id, accountId, xWorkspaceID, parentId, limit, offset)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#listBlocks")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#listBlocks")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **parentId** | **kotlin.String**| Filter to children of this block id. Omit to list root-level blocks.  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] [default to 100] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **kotlin.Int**|  | [optional] [default to 0] |

### Return type

[**BlockListResponse**](BlockListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listNoteComments"></a>
# **listNoteComments**
> CommentListResponse listNoteComments(id, accountId, xWorkspaceID)

List comments on a note.

Returns active (non-deleted) comments. When &#x60;?accountId&#x3D;&#x60; targets an external provider that supports comments (e.g. Notion), the provider is queried directly; otherwise the native store is used. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : CommentListResponse = apiInstance.listNoteComments(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#listNoteComments")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#listNoteComments")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**CommentListResponse**](CommentListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listNotes"></a>
# **listNotes**
> NoteListEnvelope listNotes(accountId, provider, xWorkspaceID, archived, parentId, tags, limit, offset, sortBy, sortOrder)

List notes across connected accounts.

Fan-out list. Returns every note visible to the caller across every connected notes provider, paginated by &#x60;limit&#x60; / &#x60;offset&#x60;. Pass &#x60;?accountId&#x3D;&#x60; or &#x60;?provider&#x3D;&#x60; to scope to a single source. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val archived : kotlin.Boolean = true // kotlin.Boolean | When `true`, return archived notes instead of active ones.
val parentId : kotlin.String = parentId_example // kotlin.String | Filter to notes nested under this parent note id.
val tags : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Filter to notes carrying every tag listed.
val limit : kotlin.Int = 56 // kotlin.Int | Max items to return. Defaults to 50.
val offset : kotlin.Int = 56 // kotlin.Int | Number of items to skip.
val sortBy : kotlin.String = sortBy_example // kotlin.String | Sort field. Provider-dependent; the native provider supports `updated_at`, `created_at`, `title`. 
val sortOrder : kotlin.String = sortOrder_example // kotlin.String | 
try {
    val result : NoteListEnvelope = apiInstance.listNotes(accountId, provider, xWorkspaceID, archived, parentId, tags, limit, offset, sortBy, sortOrder)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#listNotes")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#listNotes")
    e.printStackTrace()
}
```

### Parameters
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **provider** | **kotlin.String**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **archived** | **kotlin.Boolean**| When &#x60;true&#x60;, return archived notes instead of active ones. | [optional] [default to false] |
| **parentId** | **kotlin.String**| Filter to notes nested under this parent note id. | [optional] |
| **tags** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Filter to notes carrying every tag listed. | [optional] |
| **limit** | **kotlin.Int**| Max items to return. Defaults to 50. | [optional] [default to 50] |
| **offset** | **kotlin.Int**| Number of items to skip. | [optional] [default to 0] |
| **sortBy** | **kotlin.String**| Sort field. Provider-dependent; the native provider supports &#x60;updated_at&#x60;, &#x60;created_at&#x60;, &#x60;title&#x60;.  | [optional] [default to &quot;updated_at&quot;] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sortOrder** | **kotlin.String**|  | [optional] [default to SortOrder.desc] [enum: asc, desc] |

### Return type

[**NoteListEnvelope**](NoteListEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="moveBlock"></a>
# **moveBlock**
> SuccessFlag moveBlock(id, moveBlockRequest, accountId, xWorkspaceID)

Reparent or reorder a block.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Block id.
val moveBlockRequest : MoveBlockRequest =  // MoveBlockRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.moveBlock(id, moveBlockRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#moveBlock")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#moveBlock")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Block id. | |
| **moveBlockRequest** | [**MoveBlockRequest**](MoveBlockRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="rotateNoteShareToken"></a>
# **rotateNoteShareToken**
> ShareSettings rotateNoteShareToken(id, accountId, xWorkspaceID)

Rotate the share token, invalidating any outstanding URLs.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : ShareSettings = apiInstance.rotateNoteShareToken(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#rotateNoteShareToken")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#rotateNoteShareToken")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**ShareSettings**](ShareSettings.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateBlock"></a>
# **updateBlock**
> Block updateBlock(id, updateBlockRequest, accountId, xWorkspaceID)

Update a block (partial).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Block id.
val updateBlockRequest : UpdateBlockRequest =  // UpdateBlockRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Block = apiInstance.updateBlock(id, updateBlockRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#updateBlock")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#updateBlock")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Block id. | |
| **updateBlockRequest** | [**UpdateBlockRequest**](UpdateBlockRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Block**](Block.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateNote"></a>
# **updateNote**
> Note updateNote(id, updateNoteRequest, accountId, xWorkspaceID)

Update a note (partial).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val updateNoteRequest : UpdateNoteRequest =  // UpdateNoteRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Note = apiInstance.updateNote(id, updateNoteRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#updateNote")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#updateNote")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **updateNoteRequest** | [**UpdateNoteRequest**](UpdateNoteRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Note**](Note.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateNoteComment"></a>
# **updateNoteComment**
> CommentMutationResponse updateNoteComment(id, commentId, updateCommentRequest, accountId, xWorkspaceID)

Edit a comment.

Only the comment author can edit. The note owner can delete via &#x60;DELETE&#x60; but cannot rewrite. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val id : kotlin.String = id_example // kotlin.String | Note id.
val commentId : kotlin.String = commentId_example // kotlin.String | Comment id.
val updateCommentRequest : UpdateCommentRequest =  // UpdateCommentRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : CommentMutationResponse = apiInstance.updateNoteComment(id, commentId, updateCommentRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#updateNoteComment")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#updateNoteComment")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Note id. | |
| **commentId** | **kotlin.String**| Comment id. | |
| **updateCommentRequest** | [**UpdateCommentRequest**](UpdateCommentRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**CommentMutationResponse**](CommentMutationResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceCreateNote"></a>
# **workspaceCreateNote**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateNote(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateNote(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#workspaceCreateNote")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#workspaceCreateNote")
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

<a id="workspaceCreateNoteBlock"></a>
# **workspaceCreateNoteBlock**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateNoteBlock(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateNoteBlock(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#workspaceCreateNoteBlock")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#workspaceCreateNoteBlock")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **id** | **kotlin.String**|  | |
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

<a id="workspaceDeleteNote"></a>
# **workspaceDeleteNote**
> workspaceDeleteNote(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceDeleteNote(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#workspaceDeleteNote")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#workspaceDeleteNote")
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

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceDeleteNoteBlock"></a>
# **workspaceDeleteNoteBlock**
> workspaceDeleteNoteBlock(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceDeleteNoteBlock(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#workspaceDeleteNoteBlock")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#workspaceDeleteNoteBlock")
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

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceGetNote"></a>
# **workspaceGetNote**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetNote(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetNote(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#workspaceGetNote")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#workspaceGetNote")
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

<a id="workspaceGetNoteBlock"></a>
# **workspaceGetNoteBlock**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetNoteBlock(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetNoteBlock(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#workspaceGetNoteBlock")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#workspaceGetNoteBlock")
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

<a id="workspaceListNoteBlocks"></a>
# **workspaceListNoteBlocks**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListNoteBlocks(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListNoteBlocks(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#workspaceListNoteBlocks")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#workspaceListNoteBlocks")
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

<a id="workspaceListNotes"></a>
# **workspaceListNotes**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListNotes(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListNotes(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#workspaceListNotes")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#workspaceListNotes")
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

<a id="workspaceMoveNoteBlock"></a>
# **workspaceMoveNoteBlock**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceMoveNoteBlock(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceMoveNoteBlock(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#workspaceMoveNoteBlock")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#workspaceMoveNoteBlock")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **id** | **kotlin.String**|  | |
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

<a id="workspaceUpdateNote"></a>
# **workspaceUpdateNote**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUpdateNote(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUpdateNote(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#workspaceUpdateNote")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#workspaceUpdateNote")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **id** | **kotlin.String**|  | |
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

<a id="workspaceUpdateNoteBlock"></a>
# **workspaceUpdateNoteBlock**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUpdateNoteBlock(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = NotesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUpdateNoteBlock(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NotesApi#workspaceUpdateNoteBlock")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotesApi#workspaceUpdateNoteBlock")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **id** | **kotlin.String**|  | |
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

