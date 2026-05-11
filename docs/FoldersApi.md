# FoldersApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createEmailFolder**](FoldersApi.md#createEmailFolder) | **POST** /v1/folders | Create an email folder. |
| [**deleteEmailFolder**](FoldersApi.md#deleteEmailFolder) | **DELETE** /v1/folders/{id} | Delete an email folder. |
| [**listEmailFolders**](FoldersApi.md#listEmailFolders) | **GET** /v1/folders | List the caller&#39;s email folders. |
| [**listFolderEmails**](FoldersApi.md#listFolderEmails) | **GET** /v1/folders/{id}/emails | List emails inside a folder. |
| [**moveEmailsToFolder**](FoldersApi.md#moveEmailsToFolder) | **POST** /v1/folders/{id}/emails | Move emails into a folder. |
| [**updateEmailFolder**](FoldersApi.md#updateEmailFolder) | **PUT** /v1/folders/{id} | Update an email folder. |


<a id="createEmailFolder"></a>
# **createEmailFolder**
> EmailFolder createEmailFolder(createEmailFolderRequest)

Create an email folder.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FoldersApi()
val createEmailFolderRequest : CreateEmailFolderRequest =  // CreateEmailFolderRequest | 
try {
    val result : EmailFolder = apiInstance.createEmailFolder(createEmailFolderRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FoldersApi#createEmailFolder")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FoldersApi#createEmailFolder")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createEmailFolderRequest** | [**CreateEmailFolderRequest**](CreateEmailFolderRequest.md)|  | |

### Return type

[**EmailFolder**](EmailFolder.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteEmailFolder"></a>
# **deleteEmailFolder**
> deleteEmailFolder(id)

Delete an email folder.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FoldersApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteEmailFolder(id)
} catch (e: ClientException) {
    println("4xx response calling FoldersApi#deleteEmailFolder")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FoldersApi#deleteEmailFolder")
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

<a id="listEmailFolders"></a>
# **listEmailFolders**
> EmailFolderListResponse listEmailFolders()

List the caller&#39;s email folders.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FoldersApi()
try {
    val result : EmailFolderListResponse = apiInstance.listEmailFolders()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FoldersApi#listEmailFolders")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FoldersApi#listEmailFolders")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**EmailFolderListResponse**](EmailFolderListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listFolderEmails"></a>
# **listFolderEmails**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listFolderEmails(id)

List emails inside a folder.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FoldersApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listFolderEmails(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FoldersApi#listFolderEmails")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FoldersApi#listFolderEmails")
    e.printStackTrace()
}
```

### Parameters
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

<a id="moveEmailsToFolder"></a>
# **moveEmailsToFolder**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; moveEmailsToFolder(id, moveEmailsRequest)

Move emails into a folder.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FoldersApi()
val id : kotlin.String = id_example // kotlin.String | 
val moveEmailsRequest : MoveEmailsRequest =  // MoveEmailsRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.moveEmailsToFolder(id, moveEmailsRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FoldersApi#moveEmailsToFolder")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FoldersApi#moveEmailsToFolder")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **moveEmailsRequest** | [**MoveEmailsRequest**](MoveEmailsRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateEmailFolder"></a>
# **updateEmailFolder**
> EmailFolder updateEmailFolder(id, updateEmailFolderRequest)

Update an email folder.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = FoldersApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateEmailFolderRequest : UpdateEmailFolderRequest =  // UpdateEmailFolderRequest | 
try {
    val result : EmailFolder = apiInstance.updateEmailFolder(id, updateEmailFolderRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling FoldersApi#updateEmailFolder")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling FoldersApi#updateEmailFolder")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateEmailFolderRequest** | [**UpdateEmailFolderRequest**](UpdateEmailFolderRequest.md)|  | |

### Return type

[**EmailFolder**](EmailFolder.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

