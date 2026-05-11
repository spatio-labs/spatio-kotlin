# FilesApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**bulkDeleteFiles**](FilesApi.md#bulkDeleteFiles) | **POST** /v1/files/delete | Delete multiple files in one call. |
| [**bulkMoveFiles**](FilesApi.md#bulkMoveFiles) | **POST** /v1/files/move | Move multiple files to a target folder. |
| [**commitChunkedUpload**](FilesApi.md#commitChunkedUpload) | **POST** /v1/files/upload/chunked/commit | Finalize a chunked-upload session and create the file row. |
| [**createFileFolder**](FilesApi.md#createFileFolder) | **POST** /v1/files/folders | Create a folder. |
| [**deleteFile**](FilesApi.md#deleteFile) | **DELETE** /v1/files/{id} | Delete a file. |
| [**extractFileText**](FilesApi.md#extractFileText) | **GET** /v1/files/{id}/extract-text | Extract text content from a PDF (or other supported file). |
| [**getChunkedFileManifest**](FilesApi.md#getChunkedFileManifest) | **GET** /v1/files/{id}/manifest | Fetch the block manifest for a chunked-uploaded file. |
| [**getFile**](FilesApi.md#getFile) | **GET** /v1/files/{id} | Fetch one file&#39;s metadata. |
| [**getFileDownloadUrl**](FilesApi.md#getFileDownloadUrl) | **GET** /v1/files/{id}/download | Mint a fresh signed download URL. |
| [**initChunkedUpload**](FilesApi.md#initChunkedUpload) | **POST** /v1/files/upload/chunked/init | Begin a content-addressed chunked upload session. |
| [**listFileFolders**](FilesApi.md#listFileFolders) | **GET** /v1/files/folders | List folders across connected file providers. |
| [**listFiles**](FilesApi.md#listFiles) | **GET** /v1/files | List files across connected file providers. |
| [**listFilesAndFolders**](FilesApi.md#listFilesAndFolders) | **GET** /v1/files/list | Aggregate list of files + folders for renderer file-browser views. |
| [**moveFile**](FilesApi.md#moveFile) | **POST** /v1/files/{id}/move | Move a single file to a target folder. |
| [**searchFiles**](FilesApi.md#searchFiles) | **GET** /v1/files/search | Substring-match search across the caller&#39;s files. |
| [**updateFile**](FilesApi.md#updateFile) | **PATCH** /v1/files/{id} | Update a file&#39;s metadata (name, folder, custom fields). |
| [**uploadChunkedBlock**](FilesApi.md#uploadChunkedBlock) | **POST** /v1/files/upload/chunked/blocks | Upload one block for an open chunked-upload session. |
| [**uploadFile**](FilesApi.md#uploadFile) | **POST** /v1/files/upload | Upload a file via multipart form. |
| [**uploadFileBase64**](FilesApi.md#uploadFileBase64) | **POST** /v1/files/upload/base64 | Upload a file via JSON with base64-encoded content. |
| [**workspaceCommitChunkedUpload**](FilesApi.md#workspaceCommitChunkedUpload) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload/chunked/commit | Workspace-scoped chunked-upload commit (RBAC-protected). |
| [**workspaceCreateFileFolder**](FilesApi.md#workspaceCreateFileFolder) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/folders | Workspace-scoped create-folder (RBAC-protected). |
| [**workspaceDeleteFile**](FilesApi.md#workspaceDeleteFile) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/files/{id} | Workspace-scoped delete-file. |
| [**workspaceGetFile**](FilesApi.md#workspaceGetFile) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files/{id} | Workspace-scoped get-file. |
| [**workspaceGetFileDownload**](FilesApi.md#workspaceGetFileDownload) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files/{id}/download | Workspace-scoped signed-download URL. |
| [**workspaceGetFileManifest**](FilesApi.md#workspaceGetFileManifest) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files/{id}/manifest | Workspace-scoped chunked-file manifest. |
| [**workspaceInitChunkedUpload**](FilesApi.md#workspaceInitChunkedUpload) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload/chunked/init | Workspace-scoped chunked-upload init (RBAC-protected). |
| [**workspaceListFileFolders**](FilesApi.md#workspaceListFileFolders) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files/folders | Workspace-scoped list-folders (RBAC-protected). |
| [**workspaceListFiles**](FilesApi.md#workspaceListFiles) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files | Workspace-scoped list-files (RBAC-protected). |
| [**workspaceMoveFile**](FilesApi.md#workspaceMoveFile) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/{id}/move | Workspace-scoped move-file. |
| [**workspaceUpdateFile**](FilesApi.md#workspaceUpdateFile) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/files/{id} | Workspace-scoped update-file. |
| [**workspaceUploadChunkedBlock**](FilesApi.md#workspaceUploadChunkedBlock) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload/chunked/blocks | Workspace-scoped chunked-upload block (RBAC-protected). |
| [**workspaceUploadFile**](FilesApi.md#workspaceUploadFile) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload | Workspace-scoped multipart upload (RBAC-protected). |
| [**workspaceUploadFileBase64**](FilesApi.md#workspaceUploadFileBase64) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload/base64 | Workspace-scoped base64 upload (RBAC-protected). |


<a id="bulkDeleteFiles"></a>
# **bulkDeleteFiles**
> BulkFilesResponse bulkDeleteFiles(bulkDeleteFilesRequest)

Delete multiple files in one call.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val bulkDeleteFilesRequest : BulkDeleteFilesRequest =  // BulkDeleteFilesRequest | 
try {
    val result : BulkFilesResponse = apiInstance.bulkDeleteFiles(bulkDeleteFilesRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#bulkDeleteFiles")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#bulkDeleteFiles")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bulkDeleteFilesRequest** | [**BulkDeleteFilesRequest**](BulkDeleteFilesRequest.md)|  | |

### Return type

[**BulkFilesResponse**](BulkFilesResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="bulkMoveFiles"></a>
# **bulkMoveFiles**
> BulkFilesResponse bulkMoveFiles(bulkMoveFilesRequest)

Move multiple files to a target folder.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val bulkMoveFilesRequest : BulkMoveFilesRequest =  // BulkMoveFilesRequest | 
try {
    val result : BulkFilesResponse = apiInstance.bulkMoveFiles(bulkMoveFilesRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#bulkMoveFiles")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#bulkMoveFiles")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bulkMoveFilesRequest** | [**BulkMoveFilesRequest**](BulkMoveFilesRequest.md)|  | |

### Return type

[**BulkFilesResponse**](BulkFilesResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="commitChunkedUpload"></a>
# **commitChunkedUpload**
> CommitChunkedUploadResponse commitChunkedUpload(commitChunkedUploadRequest)

Finalize a chunked-upload session and create the file row.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val commitChunkedUploadRequest : CommitChunkedUploadRequest =  // CommitChunkedUploadRequest | 
try {
    val result : CommitChunkedUploadResponse = apiInstance.commitChunkedUpload(commitChunkedUploadRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#commitChunkedUpload")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#commitChunkedUpload")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **commitChunkedUploadRequest** | [**CommitChunkedUploadRequest**](CommitChunkedUploadRequest.md)|  | |

### Return type

[**CommitChunkedUploadResponse**](CommitChunkedUploadResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createFileFolder"></a>
# **createFileFolder**
> Folder createFileFolder(createFolderRequest, accountId, provider, xWorkspaceID)

Create a folder.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val createFolderRequest : CreateFolderRequest =  // CreateFolderRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Folder = apiInstance.createFileFolder(createFolderRequest, accountId, provider, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#createFileFolder")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#createFileFolder")
    e.printStackTrace()
}
```

### Parameters
| **createFolderRequest** | [**CreateFolderRequest**](CreateFolderRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **provider** | **kotlin.String**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Folder**](Folder.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteFile"></a>
# **deleteFile**
> deleteFile(id, accountId, xWorkspaceID)

Delete a file.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val id : kotlin.String = id_example // kotlin.String | File id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    apiInstance.deleteFile(id, accountId, xWorkspaceID)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#deleteFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#deleteFile")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| File id. | |
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

<a id="extractFileText"></a>
# **extractFileText**
> ExtractTextResult extractFileText(id, accountId, xWorkspaceID, pageStart, pageEnd, maxChars)

Extract text content from a PDF (or other supported file).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val id : kotlin.String = id_example // kotlin.String | File id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val pageStart : kotlin.Int = 56 // kotlin.Int | 
val pageEnd : kotlin.Int = 56 // kotlin.Int | 
val maxChars : kotlin.Int = 56 // kotlin.Int | Truncation limit; sets `truncated: true` when hit.
try {
    val result : ExtractTextResult = apiInstance.extractFileText(id, accountId, xWorkspaceID, pageStart, pageEnd, maxChars)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#extractFileText")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#extractFileText")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| File id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **pageStart** | **kotlin.Int**|  | [optional] |
| **pageEnd** | **kotlin.Int**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **maxChars** | **kotlin.Int**| Truncation limit; sets &#x60;truncated: true&#x60; when hit. | [optional] |

### Return type

[**ExtractTextResult**](ExtractTextResult.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getChunkedFileManifest"></a>
# **getChunkedFileManifest**
> ChunkedFileManifest getChunkedFileManifest(id, accountId, xWorkspaceID)

Fetch the block manifest for a chunked-uploaded file.

Only meaningful for files uploaded via &#x60;upload/chunked/_*&#x60;. Files uploaded via &#x60;upload&#x60; or &#x60;upload/base64&#x60; return &#x60;404&#x60;. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val id : kotlin.String = id_example // kotlin.String | File id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : ChunkedFileManifest = apiInstance.getChunkedFileManifest(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#getChunkedFileManifest")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#getChunkedFileManifest")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| File id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**ChunkedFileManifest**](ChunkedFileManifest.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getFile"></a>
# **getFile**
> SpatioFile getFile(id, accountId, xWorkspaceID)

Fetch one file&#39;s metadata.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val id : kotlin.String = id_example // kotlin.String | File id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SpatioFile = apiInstance.getFile(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#getFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#getFile")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| File id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SpatioFile**](SpatioFile.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getFileDownloadUrl"></a>
# **getFileDownloadUrl**
> DownloadFileResponse getFileDownloadUrl(id, accountId, xWorkspaceID)

Mint a fresh signed download URL.

Returns a JSON envelope with a pre-signed URL pointing at the backing storage. Clients follow the URL — the platform does not stream bytes through itself. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val id : kotlin.String = id_example // kotlin.String | File id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : DownloadFileResponse = apiInstance.getFileDownloadUrl(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#getFileDownloadUrl")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#getFileDownloadUrl")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| File id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**DownloadFileResponse**](DownloadFileResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="initChunkedUpload"></a>
# **initChunkedUpload**
> InitChunkedUploadResponse initChunkedUpload(initChunkedUploadRequest)

Begin a content-addressed chunked upload session.

Client computes per-block hashes ahead of time and submits the list. The server replies with which blocks need uploading vs. already-on-server (deduplicated). Subsequent calls upload the missing blocks via &#x60;uploadChunkedBlock&#x60;, then &#x60;commit&#x60;. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val initChunkedUploadRequest : InitChunkedUploadRequest =  // InitChunkedUploadRequest | 
try {
    val result : InitChunkedUploadResponse = apiInstance.initChunkedUpload(initChunkedUploadRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#initChunkedUpload")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#initChunkedUpload")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **initChunkedUploadRequest** | [**InitChunkedUploadRequest**](InitChunkedUploadRequest.md)|  | |

### Return type

[**InitChunkedUploadResponse**](InitChunkedUploadResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="listFileFolders"></a>
# **listFileFolders**
> FolderListEnvelope listFileFolders(accountId, provider, xWorkspaceID, parentId, workspaceId, organizationId, limit, offset)

List folders across connected file providers.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val parentId : kotlin.String = parentId_example // kotlin.String | Filter to children of this folder. Omit for root.
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val organizationId : kotlin.String = organizationId_example // kotlin.String | 
val limit : kotlin.Int = 56 // kotlin.Int | 
val offset : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : FolderListEnvelope = apiInstance.listFileFolders(accountId, provider, xWorkspaceID, parentId, workspaceId, organizationId, limit, offset)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#listFileFolders")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#listFileFolders")
    e.printStackTrace()
}
```

### Parameters
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **provider** | **kotlin.String**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **parentId** | **kotlin.String**| Filter to children of this folder. Omit for root. | [optional] |
| **workspaceId** | **kotlin.String**|  | [optional] |
| **organizationId** | **kotlin.String**|  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] [default to 50] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **kotlin.Int**|  | [optional] [default to 0] |

### Return type

[**FolderListEnvelope**](FolderListEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listFiles"></a>
# **listFiles**
> FileListEnvelope listFiles(accountId, provider, xWorkspaceID, folderId, workspaceId, organizationId, limit, offset, sortBy, sortOrder)

List files across connected file providers.

Fan-out list. Returns files from every connected file provider unless filtered by &#x60;?accountId&#x3D;&#x60; or &#x60;?provider&#x3D;&#x60;. Folder contents are scoped via &#x60;?folderId&#x3D;&#x60;; omit for account root. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val folderId : kotlin.String = folderId_example // kotlin.String | Filter to one folder. Omit for the account root.
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val organizationId : kotlin.String = organizationId_example // kotlin.String | 
val limit : kotlin.Int = 56 // kotlin.Int | 
val offset : kotlin.Int = 56 // kotlin.Int | 
val sortBy : kotlin.String = sortBy_example // kotlin.String | Provider-dependent. Common values: `created_at`, `name`, `size`.
val sortOrder : kotlin.String = sortOrder_example // kotlin.String | 
try {
    val result : FileListEnvelope = apiInstance.listFiles(accountId, provider, xWorkspaceID, folderId, workspaceId, organizationId, limit, offset, sortBy, sortOrder)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#listFiles")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#listFiles")
    e.printStackTrace()
}
```

### Parameters
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **provider** | **kotlin.String**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **folderId** | **kotlin.String**| Filter to one folder. Omit for the account root. | [optional] |
| **workspaceId** | **kotlin.String**|  | [optional] |
| **organizationId** | **kotlin.String**|  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] [default to 50] |
| **offset** | **kotlin.Int**|  | [optional] [default to 0] |
| **sortBy** | **kotlin.String**| Provider-dependent. Common values: &#x60;created_at&#x60;, &#x60;name&#x60;, &#x60;size&#x60;. | [optional] [default to &quot;created_at&quot;] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sortOrder** | **kotlin.String**|  | [optional] [default to SortOrder.DESC] [enum: ASC, DESC] |

### Return type

[**FileListEnvelope**](FileListEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listFilesAndFolders"></a>
# **listFilesAndFolders**
> FilesAndFoldersResponse listFilesAndFolders(accountId, provider, folderId, workspaceId, organizationId, limit, offset, sortBy, sortOrder)

Aggregate list of files + folders for renderer file-browser views.

Calls &#x60;listFiles&#x60; and &#x60;listFileFolders&#x60; in parallel and merges the results. Saves a round-trip when the UI shows both side-by-side. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val folderId : kotlin.String = folderId_example // kotlin.String | Filter to one folder. Omit for the account root.
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val organizationId : kotlin.String = organizationId_example // kotlin.String | 
val limit : kotlin.Int = 56 // kotlin.Int | 
val offset : kotlin.Int = 56 // kotlin.Int | 
val sortBy : kotlin.String = sortBy_example // kotlin.String | 
val sortOrder : kotlin.String = sortOrder_example // kotlin.String | 
try {
    val result : FilesAndFoldersResponse = apiInstance.listFilesAndFolders(accountId, provider, folderId, workspaceId, organizationId, limit, offset, sortBy, sortOrder)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#listFilesAndFolders")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#listFilesAndFolders")
    e.printStackTrace()
}
```

### Parameters
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **provider** | **kotlin.String**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] |
| **folderId** | **kotlin.String**| Filter to one folder. Omit for the account root. | [optional] |
| **workspaceId** | **kotlin.String**|  | [optional] |
| **organizationId** | **kotlin.String**|  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] [default to 50] |
| **offset** | **kotlin.Int**|  | [optional] [default to 0] |
| **sortBy** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sortOrder** | **kotlin.String**|  | [optional] |

### Return type

[**FilesAndFoldersResponse**](FilesAndFoldersResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="moveFile"></a>
# **moveFile**
> MoveFileResponse moveFile(id, moveFileRequest, accountId, xWorkspaceID)

Move a single file to a target folder.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val id : kotlin.String = id_example // kotlin.String | File id.
val moveFileRequest : MoveFileRequest =  // MoveFileRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : MoveFileResponse = apiInstance.moveFile(id, moveFileRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#moveFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#moveFile")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| File id. | |
| **moveFileRequest** | [**MoveFileRequest**](MoveFileRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**MoveFileResponse**](MoveFileResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="searchFiles"></a>
# **searchFiles**
> SearchFilesResponse searchFiles(query, accountId, provider, folderId, workspaceId, organizationId, limit, offset)

Substring-match search across the caller&#39;s files.

In-memory search — the platform lists up to ~500 files and filters locally on &#x60;name&#x60; (case-insensitive substring). Not suitable for global search across very large file libraries. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val query : kotlin.String = query_example // kotlin.String | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val folderId : kotlin.String = folderId_example // kotlin.String | Filter to one folder. Omit for the account root.
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val organizationId : kotlin.String = organizationId_example // kotlin.String | 
val limit : kotlin.Int = 56 // kotlin.Int | 
val offset : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : SearchFilesResponse = apiInstance.searchFiles(query, accountId, provider, folderId, workspaceId, organizationId, limit, offset)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#searchFiles")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#searchFiles")
    e.printStackTrace()
}
```

### Parameters
| **query** | **kotlin.String**|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **provider** | **kotlin.String**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] |
| **folderId** | **kotlin.String**| Filter to one folder. Omit for the account root. | [optional] |
| **workspaceId** | **kotlin.String**|  | [optional] |
| **organizationId** | **kotlin.String**|  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] [default to 50] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **kotlin.Int**|  | [optional] [default to 0] |

### Return type

[**SearchFilesResponse**](SearchFilesResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateFile"></a>
# **updateFile**
> SpatioFile updateFile(id, updateFileRequest, accountId, xWorkspaceID)

Update a file&#39;s metadata (name, folder, custom fields).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val id : kotlin.String = id_example // kotlin.String | File id.
val updateFileRequest : UpdateFileRequest =  // UpdateFileRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SpatioFile = apiInstance.updateFile(id, updateFileRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#updateFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#updateFile")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| File id. | |
| **updateFileRequest** | [**UpdateFileRequest**](UpdateFileRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SpatioFile**](SpatioFile.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="uploadChunkedBlock"></a>
# **uploadChunkedBlock**
> UploadChunkedBlockResponse uploadChunkedBlock(sessionId, blockHash, block, blockIndex)

Upload one block for an open chunked-upload session.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val sessionId : kotlin.String = sessionId_example // kotlin.String | 
val blockHash : kotlin.String = blockHash_example // kotlin.String | 
val block : java.io.File = BINARY_DATA_HERE // java.io.File | 
val blockIndex : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : UploadChunkedBlockResponse = apiInstance.uploadChunkedBlock(sessionId, blockHash, block, blockIndex)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#uploadChunkedBlock")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#uploadChunkedBlock")
    e.printStackTrace()
}
```

### Parameters
| **sessionId** | **kotlin.String**|  | |
| **blockHash** | **kotlin.String**|  | |
| **block** | **java.io.File**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockIndex** | **kotlin.Int**|  | [optional] |

### Return type

[**UploadChunkedBlockResponse**](UploadChunkedBlockResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a id="uploadFile"></a>
# **uploadFile**
> SpatioFile uploadFile(file, folderId, workspaceId, organizationId, accountId)

Upload a file via multipart form.

Multipart upload. Form field &#x60;file&#x60; carries the binary; auxiliary form fields scope the upload (&#x60;folderId&#x60;, &#x60;workspaceId&#x60;, &#x60;organizationId&#x60;, &#x60;accountId&#x60;). Max body size is currently 100 MB. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val file : java.io.File = BINARY_DATA_HERE // java.io.File | File bytes (multipart form field name `file`).
val folderId : kotlin.String = folderId_example // kotlin.String | 
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val organizationId : kotlin.String = organizationId_example // kotlin.String | 
val accountId : kotlin.String = accountId_example // kotlin.String | 
try {
    val result : SpatioFile = apiInstance.uploadFile(file, folderId, workspaceId, organizationId, accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#uploadFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#uploadFile")
    e.printStackTrace()
}
```

### Parameters
| **file** | **java.io.File**| File bytes (multipart form field name &#x60;file&#x60;). | |
| **folderId** | **kotlin.String**|  | [optional] |
| **workspaceId** | **kotlin.String**|  | [optional] |
| **organizationId** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**|  | [optional] |

### Return type

[**SpatioFile**](SpatioFile.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a id="uploadFileBase64"></a>
# **uploadFileBase64**
> SpatioFile uploadFileBase64(uploadFileBase64Request)

Upload a file via JSON with base64-encoded content.

Equivalent to &#x60;uploadFile&#x60; for clients that can&#39;t post multipart bodies (e.g. browser fetch with strict CSP). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val uploadFileBase64Request : UploadFileBase64Request =  // UploadFileBase64Request | 
try {
    val result : SpatioFile = apiInstance.uploadFileBase64(uploadFileBase64Request)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#uploadFileBase64")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#uploadFileBase64")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **uploadFileBase64Request** | [**UploadFileBase64Request**](UploadFileBase64Request.md)|  | |

### Return type

[**SpatioFile**](SpatioFile.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceCommitChunkedUpload"></a>
# **workspaceCommitChunkedUpload**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCommitChunkedUpload(org, workspace, requestBody)

Workspace-scoped chunked-upload commit (RBAC-protected).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCommitChunkedUpload(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceCommitChunkedUpload")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceCommitChunkedUpload")
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

<a id="workspaceCreateFileFolder"></a>
# **workspaceCreateFileFolder**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateFileFolder(org, workspace, requestBody)

Workspace-scoped create-folder (RBAC-protected).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateFileFolder(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceCreateFileFolder")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceCreateFileFolder")
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

<a id="workspaceDeleteFile"></a>
# **workspaceDeleteFile**
> workspaceDeleteFile(org, workspace, id)

Workspace-scoped delete-file.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceDeleteFile(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceDeleteFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceDeleteFile")
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

<a id="workspaceGetFile"></a>
# **workspaceGetFile**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetFile(org, workspace, id)

Workspace-scoped get-file.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetFile(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceGetFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceGetFile")
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

<a id="workspaceGetFileDownload"></a>
# **workspaceGetFileDownload**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetFileDownload(org, workspace, id)

Workspace-scoped signed-download URL.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetFileDownload(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceGetFileDownload")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceGetFileDownload")
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

<a id="workspaceGetFileManifest"></a>
# **workspaceGetFileManifest**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetFileManifest(org, workspace, id)

Workspace-scoped chunked-file manifest.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetFileManifest(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceGetFileManifest")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceGetFileManifest")
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

<a id="workspaceInitChunkedUpload"></a>
# **workspaceInitChunkedUpload**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceInitChunkedUpload(org, workspace, requestBody)

Workspace-scoped chunked-upload init (RBAC-protected).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceInitChunkedUpload(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceInitChunkedUpload")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceInitChunkedUpload")
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

<a id="workspaceListFileFolders"></a>
# **workspaceListFileFolders**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListFileFolders(org, workspace)

Workspace-scoped list-folders (RBAC-protected).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListFileFolders(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceListFileFolders")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceListFileFolders")
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

<a id="workspaceListFiles"></a>
# **workspaceListFiles**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListFiles(org, workspace)

Workspace-scoped list-files (RBAC-protected).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListFiles(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceListFiles")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceListFiles")
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

<a id="workspaceMoveFile"></a>
# **workspaceMoveFile**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceMoveFile(org, workspace, id, requestBody)

Workspace-scoped move-file.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceMoveFile(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceMoveFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceMoveFile")
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

<a id="workspaceUpdateFile"></a>
# **workspaceUpdateFile**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUpdateFile(org, workspace, id, requestBody)

Workspace-scoped update-file.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUpdateFile(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceUpdateFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceUpdateFile")
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

<a id="workspaceUploadChunkedBlock"></a>
# **workspaceUploadChunkedBlock**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUploadChunkedBlock(org, workspace, body)

Workspace-scoped chunked-upload block (RBAC-protected).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val body : java.io.File = BINARY_DATA_HERE // java.io.File | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUploadChunkedBlock(org, workspace, body)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceUploadChunkedBlock")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceUploadChunkedBlock")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **body** | **java.io.File**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/octet-stream
 - **Accept**: application/json

<a id="workspaceUploadFile"></a>
# **workspaceUploadFile**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUploadFile(org, workspace, file)

Workspace-scoped multipart upload (RBAC-protected).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val file : java.io.File = BINARY_DATA_HERE // java.io.File | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUploadFile(org, workspace, file)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceUploadFile")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceUploadFile")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **java.io.File**|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a id="workspaceUploadFileBase64"></a>
# **workspaceUploadFileBase64**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUploadFileBase64(org, workspace, requestBody)

Workspace-scoped base64 upload (RBAC-protected).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FilesApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUploadFileBase64(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FilesApi#workspaceUploadFileBase64")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FilesApi#workspaceUploadFileBase64")
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

