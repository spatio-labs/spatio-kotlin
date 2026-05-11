# SlidesApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createPresentation**](SlidesApi.md#createPresentation) | **POST** /v1/slides | Create a presentation. |
| [**createSlide**](SlidesApi.md#createSlide) | **POST** /v1/slides/{id}/slides | Insert a slide. |
| [**createSlideElement**](SlidesApi.md#createSlideElement) | **POST** /v1/slides/{id}/slides/{slideId}/elements | Add a canvas element (text/shape/image) to a slide. |
| [**deletePresentation**](SlidesApi.md#deletePresentation) | **DELETE** /v1/slides/{id} | Delete a presentation. |
| [**deleteSlide**](SlidesApi.md#deleteSlide) | **DELETE** /v1/slides/{id}/slides/{slideId} | Delete a slide. |
| [**deleteSlideElement**](SlidesApi.md#deleteSlideElement) | **DELETE** /v1/slides/{id}/slides/{slideId}/elements/{elementId} | Delete a slide element. |
| [**disablePresentationShare**](SlidesApi.md#disablePresentationShare) | **DELETE** /v1/slides/{id}/share | Disable public sharing. |
| [**enablePresentationShare**](SlidesApi.md#enablePresentationShare) | **POST** /v1/slides/{id}/share | Enable (or update password on) public sharing. |
| [**exportPresentationPdf**](SlidesApi.md#exportPresentationPdf) | **POST** /v1/slides/{id}/export/pdf | Render the presentation as a PDF. |
| [**exportPresentationPptx**](SlidesApi.md#exportPresentationPptx) | **POST** /v1/slides/{id}/export/pptx | Render the presentation as a PowerPoint (.pptx) file. |
| [**getPresentation**](SlidesApi.md#getPresentation) | **GET** /v1/slides/{id} | Fetch one presentation. |
| [**getPresentationShareSettings**](SlidesApi.md#getPresentationShareSettings) | **GET** /v1/slides/{id}/share | Fetch share settings for a presentation. |
| [**getPublicPresentation**](SlidesApi.md#getPublicPresentation) | **GET** /public/slides/{token} | Fetch a publicly shared presentation. |
| [**getSlide**](SlidesApi.md#getSlide) | **GET** /v1/slides/{id}/slides/{slideId} | Fetch one slide. |
| [**getSlideElement**](SlidesApi.md#getSlideElement) | **GET** /v1/slides/{id}/slides/{slideId}/elements/{elementId} | Fetch one slide element. |
| [**listPresentations**](SlidesApi.md#listPresentations) | **GET** /v1/slides | List presentations across connected accounts. |
| [**listSlideElements**](SlidesApi.md#listSlideElements) | **GET** /v1/slides/{id}/slides/{slideId}/elements | List the canvas elements on a slide. |
| [**listSlidesInPresentation**](SlidesApi.md#listSlidesInPresentation) | **GET** /v1/slides/{id}/slides | List slides in a presentation. |
| [**rotatePresentationShareToken**](SlidesApi.md#rotatePresentationShareToken) | **POST** /v1/slides/{id}/share/rotate | Rotate the share token, invalidating outstanding URLs. |
| [**updatePresentation**](SlidesApi.md#updatePresentation) | **PATCH** /v1/slides/{id} | Update presentation metadata (partial). |
| [**updateSlide**](SlidesApi.md#updateSlide) | **PATCH** /v1/slides/{id}/slides/{slideId} | Update a slide (partial). |
| [**updateSlideElement**](SlidesApi.md#updateSlideElement) | **PATCH** /v1/slides/{id}/slides/{slideId}/elements/{elementId} | Update a slide element (partial). |


<a id="createPresentation"></a>
# **createPresentation**
> Presentation createPresentation(createPresentationRequest, accountId, provider, xWorkspaceID)

Create a presentation.

Creates a new deck under the target account. Target resolution mirrors &#x60;POST /v1/notes&#x60; and &#x60;/v1/sheets&#x60;: body &#x60;accountId&#x60; → &#x60;?accountId&#x3D;&#x60; → body &#x60;provider&#x60; → &#x60;?provider&#x3D;&#x60; → caller&#39;s single connected account (errors with &#x60;ambiguous_account&#x60; otherwise). The new deck is auto-seeded with one blank slide so the renderer has something to display immediately. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val createPresentationRequest : CreatePresentationRequest =  // CreatePresentationRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Presentation = apiInstance.createPresentation(createPresentationRequest, accountId, provider, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#createPresentation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#createPresentation")
    e.printStackTrace()
}
```

### Parameters
| **createPresentationRequest** | [**CreatePresentationRequest**](CreatePresentationRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **provider** | **kotlin.String**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Presentation**](Presentation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createSlide"></a>
# **createSlide**
> Slide createSlide(id, createSlideRequest, accountId, xWorkspaceID)

Insert a slide.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val createSlideRequest : CreateSlideRequest =  // CreateSlideRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Slide = apiInstance.createSlide(id, createSlideRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#createSlide")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#createSlide")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **createSlideRequest** | [**CreateSlideRequest**](CreateSlideRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Slide**](Slide.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createSlideElement"></a>
# **createSlideElement**
> SlideElement createSlideElement(id, slideId, createSlideElementRequest, accountId, xWorkspaceID)

Add a canvas element (text/shape/image) to a slide.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val slideId : kotlin.String = slideId_example // kotlin.String | Slide id within the presentation.
val createSlideElementRequest : CreateSlideElementRequest =  // CreateSlideElementRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SlideElement = apiInstance.createSlideElement(id, slideId, createSlideElementRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#createSlideElement")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#createSlideElement")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **slideId** | **kotlin.String**| Slide id within the presentation. | |
| **createSlideElementRequest** | [**CreateSlideElementRequest**](CreateSlideElementRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SlideElement**](SlideElement.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deletePresentation"></a>
# **deletePresentation**
> SuccessFlag deletePresentation(id, accountId, xWorkspaceID)

Delete a presentation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.deletePresentation(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#deletePresentation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#deletePresentation")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
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

<a id="deleteSlide"></a>
# **deleteSlide**
> SuccessFlag deleteSlide(id, slideId, accountId, xWorkspaceID)

Delete a slide.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val slideId : kotlin.String = slideId_example // kotlin.String | Slide id within the presentation.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.deleteSlide(id, slideId, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#deleteSlide")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#deleteSlide")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **slideId** | **kotlin.String**| Slide id within the presentation. | |
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

<a id="deleteSlideElement"></a>
# **deleteSlideElement**
> SuccessFlag deleteSlideElement(id, slideId, elementId, accountId, xWorkspaceID)

Delete a slide element.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val slideId : kotlin.String = slideId_example // kotlin.String | Slide id within the presentation.
val elementId : kotlin.String = elementId_example // kotlin.String | Slide-element id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.deleteSlideElement(id, slideId, elementId, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#deleteSlideElement")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#deleteSlideElement")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **slideId** | **kotlin.String**| Slide id within the presentation. | |
| **elementId** | **kotlin.String**| Slide-element id. | |
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

<a id="disablePresentationShare"></a>
# **disablePresentationShare**
> disablePresentationShare(id, accountId, xWorkspaceID)

Disable public sharing.

Owner-only. Subsequent public viewer requests 404.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    apiInstance.disablePresentationShare(id, accountId, xWorkspaceID)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#disablePresentationShare")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#disablePresentationShare")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
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

<a id="enablePresentationShare"></a>
# **enablePresentationShare**
> ShareSettings enablePresentationShare(id, accountId, xWorkspaceID, enableShareRequest)

Enable (or update password on) public sharing.

Owner-only. With &#x60;setPassword: false&#x60; (or empty body), flips the deck public without changing the password. With &#x60;setPassword: true&#x60;, applies &#x60;password&#x60; (empty clears). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val enableShareRequest : EnableShareRequest =  // EnableShareRequest | 
try {
    val result : ShareSettings = apiInstance.enablePresentationShare(id, accountId, xWorkspaceID, enableShareRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#enablePresentationShare")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#enablePresentationShare")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
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

<a id="exportPresentationPdf"></a>
# **exportPresentationPdf**
> java.io.File exportPresentationPdf(id, accountId, xWorkspaceID, storage, filename, exportPDFRequest)

Render the presentation as a PDF.

Proxies to the Spatio export sidecar (Playwright). Two response modes selected via &#x60;?storage&#x3D;&#x60;:    - &#x60;stream&#x60; (default) — response body is the PDF binary     (&#x60;application/pdf&#x60;).   - &#x60;r2&#x60; — uploads the rendered PDF to R2 storage and returns     a JSON envelope with a 24-hour signed URL.  Returns &#x60;503 Service Unavailable&#x60; when the export sidecar is not configured (dev fallback to the client-side exporter). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val storage : kotlin.String = storage_example // kotlin.String | 
val filename : kotlin.String = filename_example // kotlin.String | Sanitized base name for the downloaded PDF.
val exportPDFRequest : ExportPDFRequest =  // ExportPDFRequest | 
try {
    val result : java.io.File = apiInstance.exportPresentationPdf(id, accountId, xWorkspaceID, storage, filename, exportPDFRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#exportPresentationPdf")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#exportPresentationPdf")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **storage** | **kotlin.String**|  | [optional] [default to Storage.stream] [enum: stream, r2] |
| **filename** | **kotlin.String**| Sanitized base name for the downloaded PDF. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **exportPDFRequest** | [**ExportPDFRequest**](ExportPDFRequest.md)|  | [optional] |

### Return type

[**java.io.File**](java.io.File.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="exportPresentationPptx"></a>
# **exportPresentationPptx**
> java.io.File exportPresentationPptx(id, accountId, xWorkspaceID, storage, filename, exportPDFRequest)

Render the presentation as a PowerPoint (.pptx) file.

Proxies to the Spatio export sidecar (Playwright + pptxgenjs). Each slide is screenshotted at 2× device-pixel ratio and wrapped into a PowerPoint .pptx as a full-bleed image. Visual fidelity is preserved exactly — what renders in Spatio renders identically in PowerPoint, Keynote, Google Slides — at the cost of in-PowerPoint editability of slide content. Users edit slide content back in Spatio (the source of truth), not inside PowerPoint.  Two response modes selected via &#x60;?storage&#x3D;&#x60;:    - &#x60;stream&#x60; (default) — response body is the PPTX binary     (&#x60;application/vnd.openxmlformats-officedocument.presentationml.presentation&#x60;).   - &#x60;r2&#x60; — uploads the rendered PPTX to R2 storage and returns     a JSON envelope with a 24-hour signed URL.  Returns &#x60;503 Service Unavailable&#x60; when the export sidecar is not configured. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val storage : kotlin.String = storage_example // kotlin.String | 
val filename : kotlin.String = filename_example // kotlin.String | Sanitized base name for the downloaded PPTX.
val exportPDFRequest : ExportPDFRequest =  // ExportPDFRequest | 
try {
    val result : java.io.File = apiInstance.exportPresentationPptx(id, accountId, xWorkspaceID, storage, filename, exportPDFRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#exportPresentationPptx")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#exportPresentationPptx")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **storage** | **kotlin.String**|  | [optional] [default to Storage.stream] [enum: stream, r2] |
| **filename** | **kotlin.String**| Sanitized base name for the downloaded PPTX. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **exportPDFRequest** | [**ExportPDFRequest**](ExportPDFRequest.md)|  | [optional] |

### Return type

[**java.io.File**](java.io.File.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="getPresentation"></a>
# **getPresentation**
> Presentation getPresentation(id, accountId, xWorkspaceID)

Fetch one presentation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Presentation = apiInstance.getPresentation(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#getPresentation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#getPresentation")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Presentation**](Presentation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getPresentationShareSettings"></a>
# **getPresentationShareSettings**
> ShareSettings getPresentationShareSettings(id, accountId, xWorkspaceID)

Fetch share settings for a presentation.

Owner-only. Mirror of &#x60;GET /v1/notes/{id}/share&#x60; — same shape, same fields. Returns the current public-share configuration, including the share token and computed public viewer URL when the deck is currently public. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : ShareSettings = apiInstance.getPresentationShareSettings(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#getPresentationShareSettings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#getPresentationShareSettings")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
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

<a id="getPublicPresentation"></a>
# **getPublicPresentation**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getPublicPresentation(token, password)

Fetch a publicly shared presentation.

Unauthenticated. Mirror of &#x60;GET /public/notes/{token}&#x60;. The share token is the credential. For password-protected decks the password is supplied via &#x60;?password&#x3D;&#x60;; the response distinguishes \&quot;no password supplied\&quot; from \&quot;wrong password\&quot; so the viewer can render the right prompt. Unknown tokens and disabled-share decks both return &#x60;404&#x60; to prevent enumeration. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val token : kotlin.String = token_example // kotlin.String | Opaque public-share token.
val password : kotlin.String = password_example // kotlin.String | Optional viewer password.
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getPublicPresentation(token, password)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#getPublicPresentation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#getPublicPresentation")
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

<a id="getSlide"></a>
# **getSlide**
> Slide getSlide(id, slideId, accountId, xWorkspaceID)

Fetch one slide.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val slideId : kotlin.String = slideId_example // kotlin.String | Slide id within the presentation.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Slide = apiInstance.getSlide(id, slideId, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#getSlide")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#getSlide")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **slideId** | **kotlin.String**| Slide id within the presentation. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Slide**](Slide.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getSlideElement"></a>
# **getSlideElement**
> SlideElement getSlideElement(id, slideId, elementId, accountId, xWorkspaceID)

Fetch one slide element.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val slideId : kotlin.String = slideId_example // kotlin.String | Slide id within the presentation.
val elementId : kotlin.String = elementId_example // kotlin.String | Slide-element id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SlideElement = apiInstance.getSlideElement(id, slideId, elementId, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#getSlideElement")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#getSlideElement")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **slideId** | **kotlin.String**| Slide id within the presentation. | |
| **elementId** | **kotlin.String**| Slide-element id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SlideElement**](SlideElement.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listPresentations"></a>
# **listPresentations**
> PresentationListEnvelope listPresentations(accountId, provider, xWorkspaceID, limit, offset)

List presentations across connected accounts.

Fan-out list. Returns every presentation visible to the caller across every connected slides provider. Pass &#x60;?accountId&#x3D;&#x60; or &#x60;?provider&#x3D;&#x60; to scope to a single source. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val limit : kotlin.Int = 56 // kotlin.Int | 
val offset : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : PresentationListEnvelope = apiInstance.listPresentations(accountId, provider, xWorkspaceID, limit, offset)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#listPresentations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#listPresentations")
    e.printStackTrace()
}
```

### Parameters
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **provider** | **kotlin.String**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] [default to 50] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **kotlin.Int**|  | [optional] [default to 0] |

### Return type

[**PresentationListEnvelope**](PresentationListEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listSlideElements"></a>
# **listSlideElements**
> SlideElementList listSlideElements(id, slideId, accountId, xWorkspaceID)

List the canvas elements on a slide.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val slideId : kotlin.String = slideId_example // kotlin.String | Slide id within the presentation.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SlideElementList = apiInstance.listSlideElements(id, slideId, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#listSlideElements")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#listSlideElements")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **slideId** | **kotlin.String**| Slide id within the presentation. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SlideElementList**](SlideElementList.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listSlidesInPresentation"></a>
# **listSlidesInPresentation**
> SlideList listSlidesInPresentation(id, accountId, xWorkspaceID)

List slides in a presentation.

Single-account list. Returns slides in the order set by their &#x60;position&#x60; field. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SlideList = apiInstance.listSlidesInPresentation(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#listSlidesInPresentation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#listSlidesInPresentation")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SlideList**](SlideList.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="rotatePresentationShareToken"></a>
# **rotatePresentationShareToken**
> ShareSettings rotatePresentationShareToken(id, accountId, xWorkspaceID)

Rotate the share token, invalidating outstanding URLs.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : ShareSettings = apiInstance.rotatePresentationShareToken(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#rotatePresentationShareToken")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#rotatePresentationShareToken")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
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

<a id="updatePresentation"></a>
# **updatePresentation**
> Presentation updatePresentation(id, updatePresentationRequest, accountId, xWorkspaceID)

Update presentation metadata (partial).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val updatePresentationRequest : UpdatePresentationRequest =  // UpdatePresentationRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Presentation = apiInstance.updatePresentation(id, updatePresentationRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#updatePresentation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#updatePresentation")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **updatePresentationRequest** | [**UpdatePresentationRequest**](UpdatePresentationRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Presentation**](Presentation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateSlide"></a>
# **updateSlide**
> Slide updateSlide(id, slideId, updateSlideRequest, accountId, xWorkspaceID)

Update a slide (partial).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val slideId : kotlin.String = slideId_example // kotlin.String | Slide id within the presentation.
val updateSlideRequest : UpdateSlideRequest =  // UpdateSlideRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Slide = apiInstance.updateSlide(id, slideId, updateSlideRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#updateSlide")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#updateSlide")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **slideId** | **kotlin.String**| Slide id within the presentation. | |
| **updateSlideRequest** | [**UpdateSlideRequest**](UpdateSlideRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Slide**](Slide.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateSlideElement"></a>
# **updateSlideElement**
> SlideElement updateSlideElement(id, slideId, elementId, updateSlideElementRequest, accountId, xWorkspaceID)

Update a slide element (partial).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SlidesApi()
val id : kotlin.String = id_example // kotlin.String | Presentation id.
val slideId : kotlin.String = slideId_example // kotlin.String | Slide id within the presentation.
val elementId : kotlin.String = elementId_example // kotlin.String | Slide-element id.
val updateSlideElementRequest : UpdateSlideElementRequest =  // UpdateSlideElementRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SlideElement = apiInstance.updateSlideElement(id, slideId, elementId, updateSlideElementRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SlidesApi#updateSlideElement")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SlidesApi#updateSlideElement")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Presentation id. | |
| **slideId** | **kotlin.String**| Slide id within the presentation. | |
| **elementId** | **kotlin.String**| Slide-element id. | |
| **updateSlideElementRequest** | [**UpdateSlideElementRequest**](UpdateSlideElementRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SlideElement**](SlideElement.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

