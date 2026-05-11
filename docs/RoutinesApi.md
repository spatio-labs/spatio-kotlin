# RoutinesApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**claimRoutineRun**](RoutinesApi.md#claimRoutineRun) | **POST** /v1/routines/runs/{id}/claim | Worker claims a queued run. |
| [**completeRoutineRun**](RoutinesApi.md#completeRoutineRun) | **POST** /v1/routines/runs/{id}/complete | Worker marks a run complete. |
| [**createRoutine**](RoutinesApi.md#createRoutine) | **POST** /v1/routines | Create a routine. |
| [**deleteRoutine**](RoutinesApi.md#deleteRoutine) | **DELETE** /v1/routines/{id} | Delete a routine. |
| [**getRoutine**](RoutinesApi.md#getRoutine) | **GET** /v1/routines/{id} | Fetch a routine. |
| [**listRoutineRuns**](RoutinesApi.md#listRoutineRuns) | **GET** /v1/routines/{id}/runs | List runs for a routine. |
| [**listRoutines**](RoutinesApi.md#listRoutines) | **GET** /v1/routines | List routines for the caller&#39;s workspace. |
| [**runRoutineNow**](RoutinesApi.md#runRoutineNow) | **POST** /v1/routines/{id}/run-now | Trigger an ad-hoc run. |
| [**updateRoutine**](RoutinesApi.md#updateRoutine) | **PATCH** /v1/routines/{id} | Update a routine. |
| [**updateRoutineRunProgress**](RoutinesApi.md#updateRoutineRunProgress) | **POST** /v1/routines/runs/{id}/progress | Worker reports progress. |


<a id="claimRoutineRun"></a>
# **claimRoutineRun**
> RoutineRun claimRoutineRun(id)

Worker claims a queued run.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RoutinesApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : RoutineRun = apiInstance.claimRoutineRun(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RoutinesApi#claimRoutineRun")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RoutinesApi#claimRoutineRun")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**RoutineRun**](RoutineRun.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="completeRoutineRun"></a>
# **completeRoutineRun**
> RoutineRun completeRoutineRun(id, routineRunCompleteRequest)

Worker marks a run complete.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RoutinesApi()
val id : kotlin.String = id_example // kotlin.String | 
val routineRunCompleteRequest : RoutineRunCompleteRequest =  // RoutineRunCompleteRequest | 
try {
    val result : RoutineRun = apiInstance.completeRoutineRun(id, routineRunCompleteRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RoutinesApi#completeRoutineRun")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RoutinesApi#completeRoutineRun")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **routineRunCompleteRequest** | [**RoutineRunCompleteRequest**](RoutineRunCompleteRequest.md)|  | |

### Return type

[**RoutineRun**](RoutineRun.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createRoutine"></a>
# **createRoutine**
> Routine createRoutine(createRoutineRequest)

Create a routine.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RoutinesApi()
val createRoutineRequest : CreateRoutineRequest =  // CreateRoutineRequest | 
try {
    val result : Routine = apiInstance.createRoutine(createRoutineRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RoutinesApi#createRoutine")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RoutinesApi#createRoutine")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createRoutineRequest** | [**CreateRoutineRequest**](CreateRoutineRequest.md)|  | |

### Return type

[**Routine**](Routine.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteRoutine"></a>
# **deleteRoutine**
> deleteRoutine(id)

Delete a routine.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RoutinesApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteRoutine(id)
} catch (e: ClientException) {
    println("4xx response calling RoutinesApi#deleteRoutine")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RoutinesApi#deleteRoutine")
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

<a id="getRoutine"></a>
# **getRoutine**
> Routine getRoutine(id)

Fetch a routine.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RoutinesApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : Routine = apiInstance.getRoutine(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RoutinesApi#getRoutine")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RoutinesApi#getRoutine")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**Routine**](Routine.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listRoutineRuns"></a>
# **listRoutineRuns**
> RoutineRunListResponse listRoutineRuns(id)

List runs for a routine.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RoutinesApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : RoutineRunListResponse = apiInstance.listRoutineRuns(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RoutinesApi#listRoutineRuns")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RoutinesApi#listRoutineRuns")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**RoutineRunListResponse**](RoutineRunListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listRoutines"></a>
# **listRoutines**
> RoutineListResponse listRoutines(workspaceId, status)

List routines for the caller&#39;s workspace.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RoutinesApi()
val workspaceId : kotlin.String = workspaceId_example // kotlin.String | 
val status : kotlin.String = status_example // kotlin.String | 
try {
    val result : RoutineListResponse = apiInstance.listRoutines(workspaceId, status)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RoutinesApi#listRoutines")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RoutinesApi#listRoutines")
    e.printStackTrace()
}
```

### Parameters
| **workspaceId** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status** | **kotlin.String**|  | [optional] |

### Return type

[**RoutineListResponse**](RoutineListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="runRoutineNow"></a>
# **runRoutineNow**
> RoutineRun runRoutineNow(id)

Trigger an ad-hoc run.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RoutinesApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : RoutineRun = apiInstance.runRoutineNow(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RoutinesApi#runRoutineNow")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RoutinesApi#runRoutineNow")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**RoutineRun**](RoutineRun.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateRoutine"></a>
# **updateRoutine**
> Routine updateRoutine(id, updateRoutineRequest)

Update a routine.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RoutinesApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateRoutineRequest : UpdateRoutineRequest =  // UpdateRoutineRequest | 
try {
    val result : Routine = apiInstance.updateRoutine(id, updateRoutineRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RoutinesApi#updateRoutine")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RoutinesApi#updateRoutine")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateRoutineRequest** | [**UpdateRoutineRequest**](UpdateRoutineRequest.md)|  | |

### Return type

[**Routine**](Routine.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateRoutineRunProgress"></a>
# **updateRoutineRunProgress**
> RoutineRun updateRoutineRunProgress(id, routineRunProgressRequest)

Worker reports progress.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RoutinesApi()
val id : kotlin.String = id_example // kotlin.String | 
val routineRunProgressRequest : RoutineRunProgressRequest =  // RoutineRunProgressRequest | 
try {
    val result : RoutineRun = apiInstance.updateRoutineRunProgress(id, routineRunProgressRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RoutinesApi#updateRoutineRunProgress")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RoutinesApi#updateRoutineRunProgress")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **routineRunProgressRequest** | [**RoutineRunProgressRequest**](RoutineRunProgressRequest.md)|  | |

### Return type

[**RoutineRun**](RoutineRun.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

