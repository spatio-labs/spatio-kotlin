# CallsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createCall**](CallsApi.md#createCall) | **POST** /v1/calls | Start a new call. |
| [**createMeetingRoom**](CallsApi.md#createMeetingRoom) | **POST** /v1/calls/rooms | Create a persistent meeting room. |
| [**deleteCallRecording**](CallsApi.md#deleteCallRecording) | **DELETE** /v1/calls/recordings/{recordingId} | Delete a recording. |
| [**endCall**](CallsApi.md#endCall) | **POST** /v1/calls/{id}/end | End a call (host only). |
| [**getBandwidthHistory**](CallsApi.md#getBandwidthHistory) | **GET** /v1/calls/bandwidth/history | Time-series bandwidth metrics. |
| [**getBandwidthSummary**](CallsApi.md#getBandwidthSummary) | **GET** /v1/calls/bandwidth/summary | Aggregate bandwidth metrics. |
| [**getCall**](CallsApi.md#getCall) | **GET** /v1/calls/{id} | Fetch a call. |
| [**getMeetingRoom**](CallsApi.md#getMeetingRoom) | **GET** /v1/calls/rooms/{id} | Fetch a meeting room. |
| [**joinCall**](CallsApi.md#joinCall) | **POST** /v1/calls/{id}/join | Join a call. |
| [**leaveCall**](CallsApi.md#leaveCall) | **POST** /v1/calls/{id}/leave | Leave a call. |
| [**listActiveCalls**](CallsApi.md#listActiveCalls) | **GET** /v1/calls | List active calls. |
| [**listCallRecordings**](CallsApi.md#listCallRecordings) | **GET** /v1/calls/{id}/recordings | List recordings for a call. |
| [**startCallRecording**](CallsApi.md#startCallRecording) | **POST** /v1/calls/{id}/recordings/start | Start a recording (host only). |
| [**stopCallRecording**](CallsApi.md#stopCallRecording) | **POST** /v1/calls/{id}/recordings/{recordingId}/stop | Stop an in-progress recording. |
| [**updateCallParticipantState**](CallsApi.md#updateCallParticipantState) | **PATCH** /v1/calls/{id}/participant | Toggle participant audio/video/screen-share state. |
| [**workspaceCreateCall**](CallsApi.md#workspaceCreateCall) | **POST** /v1/organizations/{org}/workspaces/{workspace}/calls |  |
| [**workspaceCreateMeetingRoom**](CallsApi.md#workspaceCreateMeetingRoom) | **POST** /v1/organizations/{org}/workspaces/{workspace}/calls/rooms |  |
| [**workspaceDeleteCallRecording**](CallsApi.md#workspaceDeleteCallRecording) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/calls/recordings/{recordingId} |  |
| [**workspaceEndCall**](CallsApi.md#workspaceEndCall) | **POST** /v1/organizations/{org}/workspaces/{workspace}/calls/{id}/end |  |
| [**workspaceGetBandwidthHistory**](CallsApi.md#workspaceGetBandwidthHistory) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calls/bandwidth/history |  |
| [**workspaceGetBandwidthSummary**](CallsApi.md#workspaceGetBandwidthSummary) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calls/bandwidth/summary |  |
| [**workspaceGetCall**](CallsApi.md#workspaceGetCall) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calls/{id} |  |
| [**workspaceGetMeetingRoom**](CallsApi.md#workspaceGetMeetingRoom) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calls/rooms/{id} |  |
| [**workspaceJoinCall**](CallsApi.md#workspaceJoinCall) | **POST** /v1/organizations/{org}/workspaces/{workspace}/calls/{id}/join |  |
| [**workspaceLeaveCall**](CallsApi.md#workspaceLeaveCall) | **POST** /v1/organizations/{org}/workspaces/{workspace}/calls/{id}/leave |  |
| [**workspaceListActiveCalls**](CallsApi.md#workspaceListActiveCalls) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calls |  |
| [**workspaceListCallRecordings**](CallsApi.md#workspaceListCallRecordings) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calls/{id}/recordings |  |
| [**workspaceStartCallRecording**](CallsApi.md#workspaceStartCallRecording) | **POST** /v1/organizations/{org}/workspaces/{workspace}/calls/{id}/recordings/start |  |
| [**workspaceStopCallRecording**](CallsApi.md#workspaceStopCallRecording) | **POST** /v1/organizations/{org}/workspaces/{workspace}/calls/{id}/recordings/{recordingId}/stop |  |
| [**workspaceUpdateCallParticipant**](CallsApi.md#workspaceUpdateCallParticipant) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/calls/{id}/participant |  |


<a id="createCall"></a>
# **createCall**
> SpatioCall createCall(createCallRequest)

Start a new call.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val createCallRequest : CreateCallRequest =  // CreateCallRequest | 
try {
    val result : SpatioCall = apiInstance.createCall(createCallRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#createCall")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#createCall")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createCallRequest** | [**CreateCallRequest**](CreateCallRequest.md)|  | [optional] |

### Return type

[**SpatioCall**](SpatioCall.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createMeetingRoom"></a>
# **createMeetingRoom**
> MeetingRoom createMeetingRoom(createMeetingRoomRequest)

Create a persistent meeting room.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val createMeetingRoomRequest : CreateMeetingRoomRequest =  // CreateMeetingRoomRequest | 
try {
    val result : MeetingRoom = apiInstance.createMeetingRoom(createMeetingRoomRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#createMeetingRoom")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#createMeetingRoom")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createMeetingRoomRequest** | [**CreateMeetingRoomRequest**](CreateMeetingRoomRequest.md)|  | |

### Return type

[**MeetingRoom**](MeetingRoom.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteCallRecording"></a>
# **deleteCallRecording**
> deleteCallRecording(recordingId)

Delete a recording.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val recordingId : kotlin.String = recordingId_example // kotlin.String | 
try {
    apiInstance.deleteCallRecording(recordingId)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#deleteCallRecording")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#deleteCallRecording")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **recordingId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="endCall"></a>
# **endCall**
> endCall(id)

End a call (host only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.endCall(id)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#endCall")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#endCall")
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

<a id="getBandwidthHistory"></a>
# **getBandwidthHistory**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getBandwidthHistory()

Time-series bandwidth metrics.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getBandwidthHistory()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#getBandwidthHistory")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#getBandwidthHistory")
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

<a id="getBandwidthSummary"></a>
# **getBandwidthSummary**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getBandwidthSummary()

Aggregate bandwidth metrics.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getBandwidthSummary()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#getBandwidthSummary")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#getBandwidthSummary")
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

<a id="getCall"></a>
# **getCall**
> SpatioCall getCall(id)

Fetch a call.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : SpatioCall = apiInstance.getCall(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#getCall")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#getCall")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**SpatioCall**](SpatioCall.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getMeetingRoom"></a>
# **getMeetingRoom**
> MeetingRoom getMeetingRoom(id)

Fetch a meeting room.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : MeetingRoom = apiInstance.getMeetingRoom(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#getMeetingRoom")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#getMeetingRoom")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**MeetingRoom**](MeetingRoom.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="joinCall"></a>
# **joinCall**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; joinCall(id)

Join a call.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.joinCall(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#joinCall")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#joinCall")
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

<a id="leaveCall"></a>
# **leaveCall**
> leaveCall(id)

Leave a call.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.leaveCall(id)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#leaveCall")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#leaveCall")
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

<a id="listActiveCalls"></a>
# **listActiveCalls**
> CallListResponse listActiveCalls()

List active calls.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
try {
    val result : CallListResponse = apiInstance.listActiveCalls()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#listActiveCalls")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#listActiveCalls")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**CallListResponse**](CallListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listCallRecordings"></a>
# **listCallRecordings**
> CallRecordingListResponse listCallRecordings(id)

List recordings for a call.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : CallRecordingListResponse = apiInstance.listCallRecordings(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#listCallRecordings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#listCallRecordings")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**CallRecordingListResponse**](CallRecordingListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="startCallRecording"></a>
# **startCallRecording**
> CallRecording startCallRecording(id)

Start a recording (host only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : CallRecording = apiInstance.startCallRecording(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#startCallRecording")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#startCallRecording")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**CallRecording**](CallRecording.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="stopCallRecording"></a>
# **stopCallRecording**
> CallRecording stopCallRecording(id, recordingId)

Stop an in-progress recording.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val id : kotlin.String = id_example // kotlin.String | 
val recordingId : kotlin.String = recordingId_example // kotlin.String | 
try {
    val result : CallRecording = apiInstance.stopCallRecording(id, recordingId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#stopCallRecording")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#stopCallRecording")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **recordingId** | **kotlin.String**|  | |

### Return type

[**CallRecording**](CallRecording.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateCallParticipantState"></a>
# **updateCallParticipantState**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateCallParticipantState(id, updateParticipantStateRequest)

Toggle participant audio/video/screen-share state.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateParticipantStateRequest : UpdateParticipantStateRequest =  // UpdateParticipantStateRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateCallParticipantState(id, updateParticipantStateRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#updateCallParticipantState")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#updateCallParticipantState")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateParticipantStateRequest** | [**UpdateParticipantStateRequest**](UpdateParticipantStateRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceCreateCall"></a>
# **workspaceCreateCall**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateCall(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateCall(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceCreateCall")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceCreateCall")
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

<a id="workspaceCreateMeetingRoom"></a>
# **workspaceCreateMeetingRoom**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateMeetingRoom(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateMeetingRoom(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceCreateMeetingRoom")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceCreateMeetingRoom")
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

<a id="workspaceDeleteCallRecording"></a>
# **workspaceDeleteCallRecording**
> workspaceDeleteCallRecording(org, workspace, recordingId)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val recordingId : kotlin.String = recordingId_example // kotlin.String | 
try {
    apiInstance.workspaceDeleteCallRecording(org, workspace, recordingId)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceDeleteCallRecording")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceDeleteCallRecording")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **recordingId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceEndCall"></a>
# **workspaceEndCall**
> workspaceEndCall(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceEndCall(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceEndCall")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceEndCall")
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

<a id="workspaceGetBandwidthHistory"></a>
# **workspaceGetBandwidthHistory**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetBandwidthHistory(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetBandwidthHistory(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceGetBandwidthHistory")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceGetBandwidthHistory")
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

<a id="workspaceGetBandwidthSummary"></a>
# **workspaceGetBandwidthSummary**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetBandwidthSummary(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetBandwidthSummary(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceGetBandwidthSummary")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceGetBandwidthSummary")
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

<a id="workspaceGetCall"></a>
# **workspaceGetCall**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetCall(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetCall(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceGetCall")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceGetCall")
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

<a id="workspaceGetMeetingRoom"></a>
# **workspaceGetMeetingRoom**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetMeetingRoom(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetMeetingRoom(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceGetMeetingRoom")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceGetMeetingRoom")
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

<a id="workspaceJoinCall"></a>
# **workspaceJoinCall**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceJoinCall(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceJoinCall(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceJoinCall")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceJoinCall")
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

<a id="workspaceLeaveCall"></a>
# **workspaceLeaveCall**
> workspaceLeaveCall(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceLeaveCall(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceLeaveCall")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceLeaveCall")
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

<a id="workspaceListActiveCalls"></a>
# **workspaceListActiveCalls**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListActiveCalls(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListActiveCalls(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceListActiveCalls")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceListActiveCalls")
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

<a id="workspaceListCallRecordings"></a>
# **workspaceListCallRecordings**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListCallRecordings(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListCallRecordings(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceListCallRecordings")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceListCallRecordings")
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

<a id="workspaceStartCallRecording"></a>
# **workspaceStartCallRecording**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceStartCallRecording(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceStartCallRecording(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceStartCallRecording")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceStartCallRecording")
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

<a id="workspaceStopCallRecording"></a>
# **workspaceStopCallRecording**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceStopCallRecording(org, workspace, id, recordingId)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val recordingId : kotlin.String = recordingId_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceStopCallRecording(org, workspace, id, recordingId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceStopCallRecording")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceStopCallRecording")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **recordingId** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceUpdateCallParticipant"></a>
# **workspaceUpdateCallParticipant**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUpdateCallParticipant(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CallsApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUpdateCallParticipant(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CallsApi#workspaceUpdateCallParticipant")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CallsApi#workspaceUpdateCallParticipant")
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

