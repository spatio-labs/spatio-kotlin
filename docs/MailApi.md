# MailApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**bulkArchiveEmails**](MailApi.md#bulkArchiveEmails) | **POST** /v1/mail/archive | Archive multiple messages (remove the INBOX label). |
| [**bulkDeleteEmails**](MailApi.md#bulkDeleteEmails) | **POST** /v1/mail/delete | Delete multiple messages in one call. |
| [**bulkMarkEmailsRead**](MailApi.md#bulkMarkEmailsRead) | **POST** /v1/mail/mark-read | Mark multiple messages read or unread in one call. |
| [**createDraft**](MailApi.md#createDraft) | **POST** /v1/mail/drafts | Create a draft. |
| [**createEmailLabel**](MailApi.md#createEmailLabel) | **POST** /v1/mail/labels | Create a label. |
| [**createMailTemplate**](MailApi.md#createMailTemplate) | **POST** /v1/mail/templates | Create a mail template. |
| [**deleteDraft**](MailApi.md#deleteDraft) | **DELETE** /v1/mail/drafts/{id} | Delete a draft. |
| [**deleteEmail**](MailApi.md#deleteEmail) | **DELETE** /v1/mail/email/{id} | Delete an email. |
| [**deleteEmailLabel**](MailApi.md#deleteEmailLabel) | **DELETE** /v1/mail/labels/{id} | Delete a label. |
| [**deleteMailTemplate**](MailApi.md#deleteMailTemplate) | **DELETE** /v1/mail/templates/{id} | Delete a mail template. |
| [**getEmail**](MailApi.md#getEmail) | **GET** /v1/mail/email/{id} | Fetch one email. |
| [**getEmailAttachment**](MailApi.md#getEmailAttachment) | **GET** /v1/mail/attachment/{messageId}/{attachmentId} | Download an attachment. |
| [**getEmailThread**](MailApi.md#getEmailThread) | **GET** /v1/mail/thread/{id} | Fetch a thread (the conversation a message belongs to). |
| [**getMailTemplate**](MailApi.md#getMailTemplate) | **GET** /v1/mail/templates/{id} | Fetch a mail template. |
| [**getMailThreadTracking**](MailApi.md#getMailThreadTracking) | **GET** /v1/mail/threads/{threadId}/tracking | Read mail-tracking events for a thread (open log, reply log, etc.). |
| [**instantiateMailTemplate**](MailApi.md#instantiateMailTemplate) | **POST** /v1/mail/templates/{id}/instantiate | Render a template with variables and return the resulting draft. |
| [**listDrafts**](MailApi.md#listDrafts) | **GET** /v1/mail/drafts | List drafts across connected mail accounts. |
| [**listEmailLabels**](MailApi.md#listEmailLabels) | **GET** /v1/mail/labels | List labels on the resolved mail account. |
| [**listEmails**](MailApi.md#listEmails) | **GET** /v1/mail/list | List emails across connected mail accounts. |
| [**listMailTemplates**](MailApi.md#listMailTemplates) | **GET** /v1/mail/templates | List the caller&#39;s saved mail templates. |
| [**replyEmail**](MailApi.md#replyEmail) | **POST** /v1/mail/reply | Reply to a specific email. |
| [**saveMailTemplate**](MailApi.md#saveMailTemplate) | **POST** /v1/mail/templates/save | Save-or-create endpoint used by the renderer&#39;s \&quot;save as template\&quot; flow. Distinct from POST /v1/mail/templates which is the strict create.  |
| [**searchEmails**](MailApi.md#searchEmails) | **GET** /v1/mail/search | Structured search across connected mail accounts. |
| [**sendDraft**](MailApi.md#sendDraft) | **POST** /v1/mail/drafts/{id}/send | Send a draft. |
| [**sendEmail**](MailApi.md#sendEmail) | **POST** /v1/mail/send | Send an email. |
| [**updateDraft**](MailApi.md#updateDraft) | **PUT** /v1/mail/drafts/{id} | Update a draft (full replacement of provided fields). |
| [**updateEmail**](MailApi.md#updateEmail) | **PATCH** /v1/mail/email/{id} | Update an email (mark read/star, add/remove labels). |
| [**updateMailTemplate**](MailApi.md#updateMailTemplate) | **PATCH** /v1/mail/templates/{id} | Update a mail template. |
| [**workspaceAddMailMessageLabels**](MailApi.md#workspaceAddMailMessageLabels) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/{messageId}/labels |  |
| [**workspaceCreateMailDraft**](MailApi.md#workspaceCreateMailDraft) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/drafts |  |
| [**workspaceCreateMailLabel**](MailApi.md#workspaceCreateMailLabel) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/labels |  |
| [**workspaceDeleteMail**](MailApi.md#workspaceDeleteMail) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/mail/email/{id} |  |
| [**workspaceDeleteMailDraft**](MailApi.md#workspaceDeleteMailDraft) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/mail/drafts/{id} |  |
| [**workspaceDeleteMailLabel**](MailApi.md#workspaceDeleteMailLabel) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/mail/labels/{id} |  |
| [**workspaceGetMail**](MailApi.md#workspaceGetMail) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/email/{id} |  |
| [**workspaceGetMailAttachment**](MailApi.md#workspaceGetMailAttachment) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/attachment/{messageId}/{attachmentId} |  |
| [**workspaceGetMailById**](MailApi.md#workspaceGetMailById) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/{id} | Workspace-scoped renderer-compat alias for mail/email/{id}. |
| [**workspaceGetMailDraft**](MailApi.md#workspaceGetMailDraft) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/drafts/{id} |  |
| [**workspaceGetMailThread**](MailApi.md#workspaceGetMailThread) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/thread/{id} |  |
| [**workspaceListMail**](MailApi.md#workspaceListMail) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/list |  |
| [**workspaceListMailDrafts**](MailApi.md#workspaceListMailDrafts) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/drafts |  |
| [**workspaceListMailLabels**](MailApi.md#workspaceListMailLabels) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/labels |  |
| [**workspacePatchMail**](MailApi.md#workspacePatchMail) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/mail/email/{id} |  |
| [**workspaceRemoveMailMessageLabel**](MailApi.md#workspaceRemoveMailMessageLabel) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/mail/{messageId}/labels/{labelId} |  |
| [**workspaceReplyMail**](MailApi.md#workspaceReplyMail) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/reply |  |
| [**workspaceSearchMail**](MailApi.md#workspaceSearchMail) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/search |  |
| [**workspaceSendMail**](MailApi.md#workspaceSendMail) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/send |  |
| [**workspaceSendMailDraft**](MailApi.md#workspaceSendMailDraft) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/drafts/{id}/send |  |
| [**workspaceSendMailEmailAlias**](MailApi.md#workspaceSendMailEmailAlias) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/email | Renderer-compat alias for /mail/send. |
| [**workspaceUpdateMail**](MailApi.md#workspaceUpdateMail) | **PUT** /v1/organizations/{org}/workspaces/{workspace}/mail/email/{id} |  |
| [**workspaceUpdateMailDraft**](MailApi.md#workspaceUpdateMailDraft) | **PUT** /v1/organizations/{org}/workspaces/{workspace}/mail/drafts/{id} |  |
| [**workspaceUpdateMailLabel**](MailApi.md#workspaceUpdateMailLabel) | **PUT** /v1/organizations/{org}/workspaces/{workspace}/mail/labels/{id} |  |


<a id="bulkArchiveEmails"></a>
# **bulkArchiveEmails**
> BulkArchiveResponse bulkArchiveEmails(bulkArchiveRequest)

Archive multiple messages (remove the INBOX label).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val bulkArchiveRequest : BulkArchiveRequest =  // BulkArchiveRequest | 
try {
    val result : BulkArchiveResponse = apiInstance.bulkArchiveEmails(bulkArchiveRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#bulkArchiveEmails")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#bulkArchiveEmails")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bulkArchiveRequest** | [**BulkArchiveRequest**](BulkArchiveRequest.md)|  | |

### Return type

[**BulkArchiveResponse**](BulkArchiveResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="bulkDeleteEmails"></a>
# **bulkDeleteEmails**
> BulkDeleteEmailsResponse bulkDeleteEmails(bulkDeleteEmailsRequest)

Delete multiple messages in one call.

Soft-delete by default (moves to provider trash). Set &#x60;permanent: true&#x60; for a hard delete. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val bulkDeleteEmailsRequest : BulkDeleteEmailsRequest =  // BulkDeleteEmailsRequest | 
try {
    val result : BulkDeleteEmailsResponse = apiInstance.bulkDeleteEmails(bulkDeleteEmailsRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#bulkDeleteEmails")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#bulkDeleteEmails")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bulkDeleteEmailsRequest** | [**BulkDeleteEmailsRequest**](BulkDeleteEmailsRequest.md)|  | |

### Return type

[**BulkDeleteEmailsResponse**](BulkDeleteEmailsResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="bulkMarkEmailsRead"></a>
# **bulkMarkEmailsRead**
> BulkMarkReadResponse bulkMarkEmailsRead(bulkMarkReadRequest)

Mark multiple messages read or unread in one call.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val bulkMarkReadRequest : BulkMarkReadRequest =  // BulkMarkReadRequest | 
try {
    val result : BulkMarkReadResponse = apiInstance.bulkMarkEmailsRead(bulkMarkReadRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#bulkMarkEmailsRead")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#bulkMarkEmailsRead")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bulkMarkReadRequest** | [**BulkMarkReadRequest**](BulkMarkReadRequest.md)|  | |

### Return type

[**BulkMarkReadResponse**](BulkMarkReadResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createDraft"></a>
# **createDraft**
> DraftResponse createDraft(createDraftRequest, xWorkspaceID)

Create a draft.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val createDraftRequest : CreateDraftRequest =  // CreateDraftRequest | 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : DraftResponse = apiInstance.createDraft(createDraftRequest, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#createDraft")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#createDraft")
    e.printStackTrace()
}
```

### Parameters
| **createDraftRequest** | [**CreateDraftRequest**](CreateDraftRequest.md)|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**DraftResponse**](DraftResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createEmailLabel"></a>
# **createEmailLabel**
> CreateLabelResponse createEmailLabel(createLabelRequest, accountId, xWorkspaceID)

Create a label.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val createLabelRequest : CreateLabelRequest =  // CreateLabelRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : CreateLabelResponse = apiInstance.createEmailLabel(createLabelRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#createEmailLabel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#createEmailLabel")
    e.printStackTrace()
}
```

### Parameters
| **createLabelRequest** | [**CreateLabelRequest**](CreateLabelRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**CreateLabelResponse**](CreateLabelResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createMailTemplate"></a>
# **createMailTemplate**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; createMailTemplate(requestBody)

Create a mail template.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.createMailTemplate(requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#createMailTemplate")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#createMailTemplate")
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

<a id="deleteDraft"></a>
# **deleteDraft**
> deleteDraft(id, accountId, xWorkspaceID)

Delete a draft.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val id : kotlin.String = id_example // kotlin.String | Draft id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    apiInstance.deleteDraft(id, accountId, xWorkspaceID)
} catch (e: ClientException) {
    println("4xx response calling MailApi#deleteDraft")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#deleteDraft")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Draft id. | |
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

<a id="deleteEmail"></a>
# **deleteEmail**
> SuccessFlag deleteEmail(id, accountId, xWorkspaceID)

Delete an email.

Soft-deletes (moves to provider trash).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val id : kotlin.String = id_example // kotlin.String | Email message id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.deleteEmail(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#deleteEmail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#deleteEmail")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Email message id. | |
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

<a id="deleteEmailLabel"></a>
# **deleteEmailLabel**
> deleteEmailLabel(id, accountId, xWorkspaceID)

Delete a label.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val id : kotlin.String = id_example // kotlin.String | Label id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    apiInstance.deleteEmailLabel(id, accountId, xWorkspaceID)
} catch (e: ClientException) {
    println("4xx response calling MailApi#deleteEmailLabel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#deleteEmailLabel")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Label id. | |
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

<a id="deleteMailTemplate"></a>
# **deleteMailTemplate**
> deleteMailTemplate(id)

Delete a mail template.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteMailTemplate(id)
} catch (e: ClientException) {
    println("4xx response calling MailApi#deleteMailTemplate")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#deleteMailTemplate")
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

<a id="getEmail"></a>
# **getEmail**
> GetEmailResponse getEmail(id, accountId, xWorkspaceID)

Fetch one email.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val id : kotlin.String = id_example // kotlin.String | Email message id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : GetEmailResponse = apiInstance.getEmail(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#getEmail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#getEmail")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Email message id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**GetEmailResponse**](GetEmailResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getEmailAttachment"></a>
# **getEmailAttachment**
> java.io.File getEmailAttachment(messageId, attachmentId, accountId, xWorkspaceID)

Download an attachment.

Streams the attachment binary. Response &#x60;Content-Type&#x60; matches the attachment&#39;s declared MIME type; &#x60;Content-Disposition&#x60; sets the filename. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val messageId : kotlin.String = messageId_example // kotlin.String | Message id the attachment belongs to.
val attachmentId : kotlin.String = attachmentId_example // kotlin.String | Attachment id within the message.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : java.io.File = apiInstance.getEmailAttachment(messageId, attachmentId, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#getEmailAttachment")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#getEmailAttachment")
    e.printStackTrace()
}
```

### Parameters
| **messageId** | **kotlin.String**| Message id the attachment belongs to. | |
| **attachmentId** | **kotlin.String**| Attachment id within the message. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**java.io.File**](java.io.File.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream, application/json

<a id="getEmailThread"></a>
# **getEmailThread**
> GetThreadResponse getEmailThread(id, accountId, xWorkspaceID)

Fetch a thread (the conversation a message belongs to).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val id : kotlin.String = id_example // kotlin.String | Thread id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : GetThreadResponse = apiInstance.getEmailThread(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#getEmailThread")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#getEmailThread")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Thread id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**GetThreadResponse**](GetThreadResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getMailTemplate"></a>
# **getMailTemplate**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getMailTemplate(id)

Fetch a mail template.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getMailTemplate(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#getMailTemplate")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#getMailTemplate")
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

<a id="getMailThreadTracking"></a>
# **getMailThreadTracking**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getMailThreadTracking(threadId)

Read mail-tracking events for a thread (open log, reply log, etc.).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val threadId : kotlin.String = threadId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getMailThreadTracking(threadId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#getMailThreadTracking")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#getMailThreadTracking")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **threadId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="instantiateMailTemplate"></a>
# **instantiateMailTemplate**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; instantiateMailTemplate(id, requestBody)

Render a template with variables and return the resulting draft.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.instantiateMailTemplate(id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#instantiateMailTemplate")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#instantiateMailTemplate")
    e.printStackTrace()
}
```

### Parameters
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

<a id="listDrafts"></a>
# **listDrafts**
> ListDraftsResponse listDrafts(xWorkspaceID, accountIds, providers, limit, nextPageToken)

List drafts across connected mail accounts.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val accountIds : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used. 
val providers : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`).
val limit : kotlin.Int = 56 // kotlin.Int | 
val nextPageToken : kotlin.String = nextPageToken_example // kotlin.String | 
try {
    val result : ListDraftsResponse = apiInstance.listDrafts(xWorkspaceID, accountIds, providers, limit, nextPageToken)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#listDrafts")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#listDrafts")
    e.printStackTrace()
}
```

### Parameters
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **accountIds** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] |
| **providers** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] |
| **limit** | **kotlin.Int**|  | [optional] [default to 50] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **nextPageToken** | **kotlin.String**|  | [optional] |

### Return type

[**ListDraftsResponse**](ListDraftsResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listEmailLabels"></a>
# **listEmailLabels**
> ListLabelsResponse listEmailLabels(accountId, xWorkspaceID)

List labels on the resolved mail account.

Single-account list. The platform auto-resolves to the caller&#39;s sole connected account; pass &#x60;?accountId&#x3D;&#x60; to disambiguate when multiple are connected. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : ListLabelsResponse = apiInstance.listEmailLabels(accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#listEmailLabels")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#listEmailLabels")
    e.printStackTrace()
}
```

### Parameters
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**ListLabelsResponse**](ListLabelsResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listEmails"></a>
# **listEmails**
> ListEmailsResponse listEmails(accountIds, providers, xWorkspaceID, query, labels, folder, limit, offset)

List emails across connected mail accounts.

Fan-out list. Returns messages across every connected mail provider unless filtered. Pass &#x60;?accountIds&#x3D;&#x60; (repeatable) to restrict to specific accounts, &#x60;?providers&#x3D;&#x60; to restrict to specific provider ids, or both for the intersection. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val accountIds : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used. 
val providers : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`).
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val query : kotlin.String = query_example // kotlin.String | Provider-specific full-text query (e.g. Gmail search syntax).
val labels : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Filter to messages carrying every label.
val folder : kotlin.String = folder_example // kotlin.String | Logical folder filter. Canonical values: `inbox`, `sent`, `starred`, `trash`, `archive`. Provider-specific folders accepted as opaque strings. 
val limit : kotlin.Int = 56 // kotlin.Int | 
val offset : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : ListEmailsResponse = apiInstance.listEmails(accountIds, providers, xWorkspaceID, query, labels, folder, limit, offset)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#listEmails")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#listEmails")
    e.printStackTrace()
}
```

### Parameters
| **accountIds** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] |
| **providers** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **query** | **kotlin.String**| Provider-specific full-text query (e.g. Gmail search syntax). | [optional] |
| **labels** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Filter to messages carrying every label. | [optional] |
| **folder** | **kotlin.String**| Logical folder filter. Canonical values: &#x60;inbox&#x60;, &#x60;sent&#x60;, &#x60;starred&#x60;, &#x60;trash&#x60;, &#x60;archive&#x60;. Provider-specific folders accepted as opaque strings.  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] [default to 50] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **kotlin.Int**|  | [optional] [default to 0] |

### Return type

[**ListEmailsResponse**](ListEmailsResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listMailTemplates"></a>
# **listMailTemplates**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listMailTemplates()

List the caller&#39;s saved mail templates.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listMailTemplates()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#listMailTemplates")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#listMailTemplates")
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

<a id="replyEmail"></a>
# **replyEmail**
> SendEmailResponse replyEmail(messageId, replyEmailRequest, xWorkspaceID)

Reply to a specific email.

The original message is identified by &#x60;?messageId&#x3D;&#x60;. Body defaults to the original sender as recipient — pass &#x60;to&#x60;, &#x60;cc&#x60;, &#x60;bcc&#x60; to override. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val messageId : kotlin.String = messageId_example // kotlin.String | Id of the message being replied to.
val replyEmailRequest : ReplyEmailRequest =  // ReplyEmailRequest | 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SendEmailResponse = apiInstance.replyEmail(messageId, replyEmailRequest, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#replyEmail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#replyEmail")
    e.printStackTrace()
}
```

### Parameters
| **messageId** | **kotlin.String**| Id of the message being replied to. | |
| **replyEmailRequest** | [**ReplyEmailRequest**](ReplyEmailRequest.md)|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SendEmailResponse**](SendEmailResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="saveMailTemplate"></a>
# **saveMailTemplate**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; saveMailTemplate(requestBody)

Save-or-create endpoint used by the renderer&#39;s \&quot;save as template\&quot; flow. Distinct from POST /v1/mail/templates which is the strict create. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.saveMailTemplate(requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#saveMailTemplate")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#saveMailTemplate")
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

<a id="searchEmails"></a>
# **searchEmails**
> SearchEmailsResponse searchEmails(q, accountIds, providers, xWorkspaceID, from, to, subject, hasAttachment, isUnread, isStarred, labels, after, before, limit, nextPageToken)

Structured search across connected mail accounts.

Fan-out search. Mirrors &#x60;listEmails&#x60;&#39;s account/provider filter semantics. Date range filters are inclusive. The query string itself is passed via &#x60;?q&#x3D;&#x60; (not &#x60;?query&#x3D;&#x60;); structured filters go in their own params. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val q : kotlin.String = q_example // kotlin.String | Provider-specific full-text query string.
val accountIds : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used. 
val providers : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`).
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val from : kotlin.String = from_example // kotlin.String | 
val to : kotlin.String = to_example // kotlin.String | 
val subject : kotlin.String = subject_example // kotlin.String | 
val hasAttachment : kotlin.Boolean = true // kotlin.Boolean | 
val isUnread : kotlin.Boolean = true // kotlin.Boolean | 
val isStarred : kotlin.Boolean = true // kotlin.Boolean | 
val labels : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | 
val after : java.time.OffsetDateTime = 2013-10-20T19:20:30+01:00 // java.time.OffsetDateTime | Inclusive lower-bound date.
val before : java.time.OffsetDateTime = 2013-10-20T19:20:30+01:00 // java.time.OffsetDateTime | Inclusive upper-bound date.
val limit : kotlin.Int = 56 // kotlin.Int | 
val nextPageToken : kotlin.String = nextPageToken_example // kotlin.String | Cursor returned by the previous call.
try {
    val result : SearchEmailsResponse = apiInstance.searchEmails(q, accountIds, providers, xWorkspaceID, from, to, subject, hasAttachment, isUnread, isStarred, labels, after, before, limit, nextPageToken)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#searchEmails")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#searchEmails")
    e.printStackTrace()
}
```

### Parameters
| **q** | **kotlin.String**| Provider-specific full-text query string. | |
| **accountIds** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] |
| **providers** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **from** | **kotlin.String**|  | [optional] |
| **to** | **kotlin.String**|  | [optional] |
| **subject** | **kotlin.String**|  | [optional] |
| **hasAttachment** | **kotlin.Boolean**|  | [optional] |
| **isUnread** | **kotlin.Boolean**|  | [optional] |
| **isStarred** | **kotlin.Boolean**|  | [optional] |
| **labels** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)|  | [optional] |
| **after** | **java.time.OffsetDateTime**| Inclusive lower-bound date. | [optional] |
| **before** | **java.time.OffsetDateTime**| Inclusive upper-bound date. | [optional] |
| **limit** | **kotlin.Int**|  | [optional] [default to 50] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **nextPageToken** | **kotlin.String**| Cursor returned by the previous call. | [optional] |

### Return type

[**SearchEmailsResponse**](SearchEmailsResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="sendDraft"></a>
# **sendDraft**
> SendEmailResponse sendDraft(id, accountId, xWorkspaceID)

Send a draft.

Submits the draft as an outbound message. The draft is consumed by the provider — subsequent &#x60;getDraft&#x60;/&#x60;updateDraft&#x60; calls return &#x60;404&#x60;. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val id : kotlin.String = id_example // kotlin.String | Draft id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SendEmailResponse = apiInstance.sendDraft(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#sendDraft")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#sendDraft")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Draft id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SendEmailResponse**](SendEmailResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="sendEmail"></a>
# **sendEmail**
> SendEmailResponse sendEmail(sendEmailRequest, xWorkspaceID)

Send an email.

Sends through the resolved connected account (auto-picks if the caller has exactly one connected mail account; errors &#x60;ambiguous_account&#x60; otherwise unless &#x60;accountId&#x60; is supplied). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val sendEmailRequest : SendEmailRequest =  // SendEmailRequest | 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SendEmailResponse = apiInstance.sendEmail(sendEmailRequest, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#sendEmail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#sendEmail")
    e.printStackTrace()
}
```

### Parameters
| **sendEmailRequest** | [**SendEmailRequest**](SendEmailRequest.md)|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SendEmailResponse**](SendEmailResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateDraft"></a>
# **updateDraft**
> DraftResponse updateDraft(id, updateDraftRequest, accountId, xWorkspaceID)

Update a draft (full replacement of provided fields).

PUT replaces the full set of provided fields on the draft. Fields omitted from the body are not modified. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val id : kotlin.String = id_example // kotlin.String | Draft id.
val updateDraftRequest : UpdateDraftRequest =  // UpdateDraftRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : DraftResponse = apiInstance.updateDraft(id, updateDraftRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#updateDraft")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#updateDraft")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Draft id. | |
| **updateDraftRequest** | [**UpdateDraftRequest**](UpdateDraftRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**DraftResponse**](DraftResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateEmail"></a>
# **updateEmail**
> UpdateEmailResponse updateEmail(id, updateEmailRequest, accountId, xWorkspaceID)

Update an email (mark read/star, add/remove labels).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val id : kotlin.String = id_example // kotlin.String | Email message id.
val updateEmailRequest : UpdateEmailRequest =  // UpdateEmailRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : UpdateEmailResponse = apiInstance.updateEmail(id, updateEmailRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#updateEmail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#updateEmail")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Email message id. | |
| **updateEmailRequest** | [**UpdateEmailRequest**](UpdateEmailRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**UpdateEmailResponse**](UpdateEmailResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateMailTemplate"></a>
# **updateMailTemplate**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateMailTemplate(id, requestBody)

Update a mail template.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateMailTemplate(id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#updateMailTemplate")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#updateMailTemplate")
    e.printStackTrace()
}
```

### Parameters
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

<a id="workspaceAddMailMessageLabels"></a>
# **workspaceAddMailMessageLabels**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceAddMailMessageLabels(org, workspace, messageId, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val messageId : kotlin.String = messageId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceAddMailMessageLabels(org, workspace, messageId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceAddMailMessageLabels")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceAddMailMessageLabels")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
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

<a id="workspaceCreateMailDraft"></a>
# **workspaceCreateMailDraft**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateMailDraft(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateMailDraft(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceCreateMailDraft")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceCreateMailDraft")
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

<a id="workspaceCreateMailLabel"></a>
# **workspaceCreateMailLabel**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateMailLabel(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateMailLabel(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceCreateMailLabel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceCreateMailLabel")
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

<a id="workspaceDeleteMail"></a>
# **workspaceDeleteMail**
> workspaceDeleteMail(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceDeleteMail(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceDeleteMail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceDeleteMail")
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

<a id="workspaceDeleteMailDraft"></a>
# **workspaceDeleteMailDraft**
> workspaceDeleteMailDraft(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceDeleteMailDraft(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceDeleteMailDraft")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceDeleteMailDraft")
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

<a id="workspaceDeleteMailLabel"></a>
# **workspaceDeleteMailLabel**
> workspaceDeleteMailLabel(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceDeleteMailLabel(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceDeleteMailLabel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceDeleteMailLabel")
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

<a id="workspaceGetMail"></a>
# **workspaceGetMail**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetMail(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetMail(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceGetMail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceGetMail")
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

<a id="workspaceGetMailAttachment"></a>
# **workspaceGetMailAttachment**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetMailAttachment(org, workspace, messageId, attachmentId)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val messageId : kotlin.String = messageId_example // kotlin.String | 
val attachmentId : kotlin.String = attachmentId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetMailAttachment(org, workspace, messageId, attachmentId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceGetMailAttachment")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceGetMailAttachment")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **messageId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **attachmentId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceGetMailById"></a>
# **workspaceGetMailById**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetMailById(org, workspace, id)

Workspace-scoped renderer-compat alias for mail/email/{id}.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetMailById(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceGetMailById")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceGetMailById")
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

<a id="workspaceGetMailDraft"></a>
# **workspaceGetMailDraft**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetMailDraft(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetMailDraft(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceGetMailDraft")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceGetMailDraft")
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

<a id="workspaceGetMailThread"></a>
# **workspaceGetMailThread**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetMailThread(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetMailThread(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceGetMailThread")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceGetMailThread")
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

<a id="workspaceListMail"></a>
# **workspaceListMail**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListMail(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListMail(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceListMail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceListMail")
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

<a id="workspaceListMailDrafts"></a>
# **workspaceListMailDrafts**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListMailDrafts(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListMailDrafts(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceListMailDrafts")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceListMailDrafts")
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

<a id="workspaceListMailLabels"></a>
# **workspaceListMailLabels**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListMailLabels(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListMailLabels(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceListMailLabels")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceListMailLabels")
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

<a id="workspacePatchMail"></a>
# **workspacePatchMail**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspacePatchMail(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspacePatchMail(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspacePatchMail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspacePatchMail")
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

<a id="workspaceRemoveMailMessageLabel"></a>
# **workspaceRemoveMailMessageLabel**
> workspaceRemoveMailMessageLabel(org, workspace, messageId, labelId)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val messageId : kotlin.String = messageId_example // kotlin.String | 
val labelId : kotlin.String = labelId_example // kotlin.String | 
try {
    apiInstance.workspaceRemoveMailMessageLabel(org, workspace, messageId, labelId)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceRemoveMailMessageLabel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceRemoveMailMessageLabel")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **messageId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **labelId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceReplyMail"></a>
# **workspaceReplyMail**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceReplyMail(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceReplyMail(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceReplyMail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceReplyMail")
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

<a id="workspaceSearchMail"></a>
# **workspaceSearchMail**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceSearchMail(org, workspace, q)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val q : kotlin.String = q_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceSearchMail(org, workspace, q)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceSearchMail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceSearchMail")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
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

<a id="workspaceSendMail"></a>
# **workspaceSendMail**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceSendMail(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceSendMail(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceSendMail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceSendMail")
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

<a id="workspaceSendMailDraft"></a>
# **workspaceSendMailDraft**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceSendMailDraft(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceSendMailDraft(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceSendMailDraft")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceSendMailDraft")
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

<a id="workspaceSendMailEmailAlias"></a>
# **workspaceSendMailEmailAlias**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceSendMailEmailAlias(org, workspace, requestBody)

Renderer-compat alias for /mail/send.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceSendMailEmailAlias(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceSendMailEmailAlias")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceSendMailEmailAlias")
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

<a id="workspaceUpdateMail"></a>
# **workspaceUpdateMail**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUpdateMail(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUpdateMail(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceUpdateMail")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceUpdateMail")
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

<a id="workspaceUpdateMailDraft"></a>
# **workspaceUpdateMailDraft**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUpdateMailDraft(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUpdateMailDraft(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceUpdateMailDraft")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceUpdateMailDraft")
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

<a id="workspaceUpdateMailLabel"></a>
# **workspaceUpdateMailLabel**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUpdateMailLabel(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = MailApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUpdateMailLabel(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MailApi#workspaceUpdateMailLabel")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MailApi#workspaceUpdateMailLabel")
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

