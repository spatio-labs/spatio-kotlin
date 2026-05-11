# SheetsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createSheet**](SheetsApi.md#createSheet) | **POST** /v1/sheets | Create a sheet. |
| [**createSheetRow**](SheetsApi.md#createSheetRow) | **POST** /v1/sheets/{id}/rows | Insert a row. |
| [**deleteSheet**](SheetsApi.md#deleteSheet) | **DELETE** /v1/sheets/{id} | Delete a sheet. |
| [**deleteSheetRow**](SheetsApi.md#deleteSheetRow) | **DELETE** /v1/sheets/{id}/rows/{rowIndex} | Delete a row. |
| [**getSheet**](SheetsApi.md#getSheet) | **GET** /v1/sheets/{id} | Fetch one sheet. |
| [**listSheetRows**](SheetsApi.md#listSheetRows) | **GET** /v1/sheets/{id}/rows | List rows in a sheet. |
| [**listSheets**](SheetsApi.md#listSheets) | **GET** /v1/sheets | List sheets across connected accounts. |
| [**updateSheet**](SheetsApi.md#updateSheet) | **PATCH** /v1/sheets/{id} | Update a sheet (partial). |
| [**updateSheetCell**](SheetsApi.md#updateSheetCell) | **PATCH** /v1/sheets/{id}/rows/{rowIndex}/cells/{column} | Update a single cell. |
| [**updateSheetRow**](SheetsApi.md#updateSheetRow) | **PATCH** /v1/sheets/{id}/rows/{rowIndex} | Update a row (sparse). |


<a id="createSheet"></a>
# **createSheet**
> Sheet createSheet(createSheetRequest, accountId, provider, xWorkspaceID)

Create a sheet.

Creates a new sheet under the target account. Target resolution mirrors &#x60;POST /v1/notes&#x60;: body &#x60;accountId&#x60; → &#x60;?accountId&#x3D;&#x60; → body &#x60;provider&#x60; → &#x60;?provider&#x3D;&#x60; → caller&#39;s single connected account (errors with &#x60;ambiguous_account&#x60; if more than one is connected and no selector is supplied). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SheetsApi()
val createSheetRequest : CreateSheetRequest =  // CreateSheetRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Sheet = apiInstance.createSheet(createSheetRequest, accountId, provider, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SheetsApi#createSheet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SheetsApi#createSheet")
    e.printStackTrace()
}
```

### Parameters
| **createSheetRequest** | [**CreateSheetRequest**](CreateSheetRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **provider** | **kotlin.String**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Sheet**](Sheet.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createSheetRow"></a>
# **createSheetRow**
> Row createSheetRow(id, createRowRequest, accountId, xWorkspaceID)

Insert a row.

Inserts a row at &#x60;index&#x60; (zero-based) or appends to the end when &#x60;index&#x60; is omitted. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SheetsApi()
val id : kotlin.String = id_example // kotlin.String | Sheet id.
val createRowRequest : CreateRowRequest =  // CreateRowRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Row = apiInstance.createSheetRow(id, createRowRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SheetsApi#createSheetRow")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SheetsApi#createSheetRow")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Sheet id. | |
| **createRowRequest** | [**CreateRowRequest**](CreateRowRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Row**](Row.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteSheet"></a>
# **deleteSheet**
> SuccessFlag deleteSheet(id, accountId, xWorkspaceID)

Delete a sheet.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SheetsApi()
val id : kotlin.String = id_example // kotlin.String | Sheet id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.deleteSheet(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SheetsApi#deleteSheet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SheetsApi#deleteSheet")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Sheet id. | |
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

<a id="deleteSheetRow"></a>
# **deleteSheetRow**
> SuccessFlag deleteSheetRow(id, rowIndex, accountId, xWorkspaceID)

Delete a row.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SheetsApi()
val id : kotlin.String = id_example // kotlin.String | Sheet id.
val rowIndex : kotlin.Int = 56 // kotlin.Int | Zero-based row index.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SuccessFlag = apiInstance.deleteSheetRow(id, rowIndex, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SheetsApi#deleteSheetRow")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SheetsApi#deleteSheetRow")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Sheet id. | |
| **rowIndex** | **kotlin.Int**| Zero-based row index. | |
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

<a id="getSheet"></a>
# **getSheet**
> Sheet getSheet(id, accountId, xWorkspaceID)

Fetch one sheet.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SheetsApi()
val id : kotlin.String = id_example // kotlin.String | Sheet id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Sheet = apiInstance.getSheet(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SheetsApi#getSheet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SheetsApi#getSheet")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Sheet id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Sheet**](Sheet.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listSheetRows"></a>
# **listSheetRows**
> RowList listSheetRows(id, accountId, xWorkspaceID, limit, offset)

List rows in a sheet.

Single-account row list. Unlike &#x60;GET /v1/sheets&#x60;, row listing always targets the one account that owns the sheet, so the response is a plain &#x60;{ rows, total }&#x60; rather than a fan-out envelope. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SheetsApi()
val id : kotlin.String = id_example // kotlin.String | Sheet id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val limit : kotlin.Int = 56 // kotlin.Int | 
val offset : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : RowList = apiInstance.listSheetRows(id, accountId, xWorkspaceID, limit, offset)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SheetsApi#listSheetRows")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SheetsApi#listSheetRows")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Sheet id. | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **limit** | **kotlin.Int**|  | [optional] [default to 100] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **kotlin.Int**|  | [optional] [default to 0] |

### Return type

[**RowList**](RowList.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listSheets"></a>
# **listSheets**
> SheetListEnvelope listSheets(accountId, provider, xWorkspaceID, limit, offset)

List sheets across connected accounts.

Fan-out list. Returns every sheet visible to the caller across every connected sheets provider, paginated by &#x60;limit&#x60; / &#x60;offset&#x60;. Pass &#x60;?accountId&#x3D;&#x60; or &#x60;?provider&#x3D;&#x60; to scope to a single source. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SheetsApi()
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val provider : kotlin.String = provider_example // kotlin.String | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val limit : kotlin.Int = 56 // kotlin.Int | 
val offset : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : SheetListEnvelope = apiInstance.listSheets(accountId, provider, xWorkspaceID, limit, offset)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SheetsApi#listSheets")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SheetsApi#listSheets")
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

[**SheetListEnvelope**](SheetListEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateSheet"></a>
# **updateSheet**
> Sheet updateSheet(id, updateSheetRequest, accountId, xWorkspaceID)

Update a sheet (partial).

Partial update of sheet metadata. The renderer also calls this via &#x60;PUT /v1/sheets/{id}&#x60; for autosave parity; both verbs invoke the same handler. Per-cell and per-row mutations live on their dedicated endpoints, not here. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SheetsApi()
val id : kotlin.String = id_example // kotlin.String | Sheet id.
val updateSheetRequest : UpdateSheetRequest =  // UpdateSheetRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Sheet = apiInstance.updateSheet(id, updateSheetRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SheetsApi#updateSheet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SheetsApi#updateSheet")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Sheet id. | |
| **updateSheetRequest** | [**UpdateSheetRequest**](UpdateSheetRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Sheet**](Sheet.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateSheetCell"></a>
# **updateSheetCell**
> Cell updateSheetCell(id, rowIndex, column, updateCellRequest, accountId, xWorkspaceID)

Update a single cell.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SheetsApi()
val id : kotlin.String = id_example // kotlin.String | Sheet id.
val rowIndex : kotlin.Int = 56 // kotlin.Int | Zero-based row index.
val column : kotlin.String = column_example // kotlin.String | Column identifier. Provider-specific — usually a letter (`A`, `AB`) for spreadsheet providers or a column key string for structured providers. 
val updateCellRequest : UpdateCellRequest =  // UpdateCellRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Cell = apiInstance.updateSheetCell(id, rowIndex, column, updateCellRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SheetsApi#updateSheetCell")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SheetsApi#updateSheetCell")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Sheet id. | |
| **rowIndex** | **kotlin.Int**| Zero-based row index. | |
| **column** | **kotlin.String**| Column identifier. Provider-specific — usually a letter (&#x60;A&#x60;, &#x60;AB&#x60;) for spreadsheet providers or a column key string for structured providers.  | |
| **updateCellRequest** | [**UpdateCellRequest**](UpdateCellRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Cell**](Cell.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateSheetRow"></a>
# **updateSheetRow**
> Row updateSheetRow(id, rowIndex, updateRowRequest, accountId, xWorkspaceID)

Update a row (sparse).

Sparse update — keys present in &#x60;cells&#x60; overwrite that column; keys absent are preserved. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = SheetsApi()
val id : kotlin.String = id_example // kotlin.String | Sheet id.
val rowIndex : kotlin.Int = 56 // kotlin.Int | Zero-based row index.
val updateRowRequest : UpdateRowRequest =  // UpdateRowRequest | 
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : Row = apiInstance.updateSheetRow(id, rowIndex, updateRowRequest, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SheetsApi#updateSheetRow")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SheetsApi#updateSheetRow")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Sheet id. | |
| **rowIndex** | **kotlin.Int**| Zero-based row index. | |
| **updateRowRequest** | [**UpdateRowRequest**](UpdateRowRequest.md)|  | |
| **accountId** | **kotlin.String**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**Row**](Row.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

