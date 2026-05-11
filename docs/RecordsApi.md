# RecordsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createRecord**](RecordsApi.md#createRecord) | **POST** /v1/records | Create a record. |
| [**createRecordType**](RecordsApi.md#createRecordType) | **POST** /v1/records/types | Create a record type (org-scoped). |
| [**deleteRecord**](RecordsApi.md#deleteRecord) | **DELETE** /v1/records/{id} | Delete a record. |
| [**getRecord**](RecordsApi.md#getRecord) | **GET** /v1/records/{id} | Fetch a record. |
| [**listRecordTypes**](RecordsApi.md#listRecordTypes) | **GET** /v1/records/types | List record types for an organization. |
| [**listRecords**](RecordsApi.md#listRecords) | **GET** /v1/records | List records for an organization. &#x60;organization_id&#x60; query param is required (handler returns 400 otherwise).  |
| [**updateRecord**](RecordsApi.md#updateRecord) | **PATCH** /v1/records/{id} | Update a record. |
| [**updateRecordType**](RecordsApi.md#updateRecordType) | **PATCH** /v1/records/types/{id} | Update a record type. |


<a id="createRecord"></a>
# **createRecord**
> Record createRecord(createRecordRequest)

Create a record.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecordsApi()
val createRecordRequest : CreateRecordRequest =  // CreateRecordRequest | 
try {
    val result : Record = apiInstance.createRecord(createRecordRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RecordsApi#createRecord")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecordsApi#createRecord")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createRecordRequest** | [**CreateRecordRequest**](CreateRecordRequest.md)|  | |

### Return type

[**Record**](Record.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createRecordType"></a>
# **createRecordType**
> RecordType createRecordType(createRecordTypeRequest)

Create a record type (org-scoped).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecordsApi()
val createRecordTypeRequest : CreateRecordTypeRequest =  // CreateRecordTypeRequest | 
try {
    val result : RecordType = apiInstance.createRecordType(createRecordTypeRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RecordsApi#createRecordType")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecordsApi#createRecordType")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createRecordTypeRequest** | [**CreateRecordTypeRequest**](CreateRecordTypeRequest.md)|  | |

### Return type

[**RecordType**](RecordType.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteRecord"></a>
# **deleteRecord**
> deleteRecord(id)

Delete a record.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecordsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteRecord(id)
} catch (e: ClientException) {
    println("4xx response calling RecordsApi#deleteRecord")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecordsApi#deleteRecord")
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

<a id="getRecord"></a>
# **getRecord**
> Record getRecord(id)

Fetch a record.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecordsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : Record = apiInstance.getRecord(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RecordsApi#getRecord")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecordsApi#getRecord")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**Record**](Record.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listRecordTypes"></a>
# **listRecordTypes**
> RecordTypeListResponse listRecordTypes(organizationId)

List record types for an organization.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecordsApi()
val organizationId : kotlin.String = organizationId_example // kotlin.String | 
try {
    val result : RecordTypeListResponse = apiInstance.listRecordTypes(organizationId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RecordsApi#listRecordTypes")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecordsApi#listRecordTypes")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organizationId** | **kotlin.String**|  | |

### Return type

[**RecordTypeListResponse**](RecordTypeListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listRecords"></a>
# **listRecords**
> RecordListResponse listRecords(organizationId, recordTypeId, limit)

List records for an organization. &#x60;organization_id&#x60; query param is required (handler returns 400 otherwise). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecordsApi()
val organizationId : kotlin.String = organizationId_example // kotlin.String | 
val recordTypeId : kotlin.String = recordTypeId_example // kotlin.String | 
val limit : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : RecordListResponse = apiInstance.listRecords(organizationId, recordTypeId, limit)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RecordsApi#listRecords")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecordsApi#listRecords")
    e.printStackTrace()
}
```

### Parameters
| **organizationId** | **kotlin.String**|  | |
| **recordTypeId** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **kotlin.Int**|  | [optional] |

### Return type

[**RecordListResponse**](RecordListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateRecord"></a>
# **updateRecord**
> Record updateRecord(id, updateRecordRequest)

Update a record.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecordsApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateRecordRequest : UpdateRecordRequest =  // UpdateRecordRequest | 
try {
    val result : Record = apiInstance.updateRecord(id, updateRecordRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RecordsApi#updateRecord")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecordsApi#updateRecord")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateRecordRequest** | [**UpdateRecordRequest**](UpdateRecordRequest.md)|  | |

### Return type

[**Record**](Record.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateRecordType"></a>
# **updateRecordType**
> RecordType updateRecordType(id, updateRecordTypeRequest)

Update a record type.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RecordsApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateRecordTypeRequest : UpdateRecordTypeRequest =  // UpdateRecordTypeRequest | 
try {
    val result : RecordType = apiInstance.updateRecordType(id, updateRecordTypeRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RecordsApi#updateRecordType")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RecordsApi#updateRecordType")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateRecordTypeRequest** | [**UpdateRecordTypeRequest**](UpdateRecordTypeRequest.md)|  | |

### Return type

[**RecordType**](RecordType.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

