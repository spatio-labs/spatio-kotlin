# CalendarApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createCalendarEvent**](CalendarApi.md#createCalendarEvent) | **POST** /v1/calendar/events | Create a calendar event. |
| [**deleteCalendarEvent**](CalendarApi.md#deleteCalendarEvent) | **DELETE** /v1/calendar/events/{id} | Delete an event. |
| [**getCalendarCapabilities**](CalendarApi.md#getCalendarCapabilities) | **GET** /v1/calendar/capabilities | Per-account capability flags. |
| [**getCalendarEvent**](CalendarApi.md#getCalendarEvent) | **GET** /v1/calendar/events/{id} | Fetch one event. |
| [**listCalendarEvents**](CalendarApi.md#listCalendarEvents) | **GET** /v1/calendar/events | List calendar events across connected accounts. |
| [**listCalendarProviders**](CalendarApi.md#listCalendarProviders) | **GET** /v1/calendar/providers | List supported calendar providers. |
| [**syncCalendar**](CalendarApi.md#syncCalendar) | **POST** /v1/calendar/sync | Trigger a sync across connected calendar accounts. |
| [**updateCalendarEvent**](CalendarApi.md#updateCalendarEvent) | **PATCH** /v1/calendar/events/{id} | Update an event (sparse). |
| [**workspaceCreateCalendarEvent**](CalendarApi.md#workspaceCreateCalendarEvent) | **POST** /v1/organizations/{org}/workspaces/{workspace}/calendar/events | Workspace-scoped create-event (RBAC-protected). |
| [**workspaceDeleteCalendarEvent**](CalendarApi.md#workspaceDeleteCalendarEvent) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/calendar/events/{id} |  |
| [**workspaceGetCalendarEvent**](CalendarApi.md#workspaceGetCalendarEvent) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calendar/events/{id} |  |
| [**workspaceListCalendarEvents**](CalendarApi.md#workspaceListCalendarEvents) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calendar/events | Workspace-scoped list-events (RBAC-protected). |
| [**workspaceListCalendarProviders**](CalendarApi.md#workspaceListCalendarProviders) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calendar/providers | Workspace-scoped calendar providers. |
| [**workspaceUpdateCalendarEvent**](CalendarApi.md#workspaceUpdateCalendarEvent) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/calendar/events/{id} |  |


<a id="createCalendarEvent"></a>
# **createCalendarEvent**
> CreateCalendarEvent201Response createCalendarEvent(createEventRequest, xWorkspaceID)

Create a calendar event.

Single-account create. &#x60;account_id&#x60; is required (no auto-resolve for write operations). Reminder array is mirrored into native tasks under the hood; conference data is auto-attached when &#x60;conference_type&#x60; is supplied. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val createEventRequest : CreateEventRequest =  // CreateEventRequest | 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : CreateCalendarEvent201Response = apiInstance.createCalendarEvent(createEventRequest, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#createCalendarEvent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#createCalendarEvent")
    e.printStackTrace()
}
```

### Parameters
| **createEventRequest** | [**CreateEventRequest**](CreateEventRequest.md)|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**CreateCalendarEvent201Response**](CreateCalendarEvent201Response.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteCalendarEvent"></a>
# **deleteCalendarEvent**
> CalendarOperationResult deleteCalendarEvent(id, accountId, xWorkspaceID)

Delete an event.

Hard delete (no soft-delete / trash). Cascades to any reminder tasks the platform created from this event. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val id : kotlin.String = id_example // kotlin.String | Event id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses `accountId`). Required for single-event operations. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : CalendarOperationResult = apiInstance.deleteCalendarEvent(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#deleteCalendarEvent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#deleteCalendarEvent")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Event id. | |
| **accountId** | **kotlin.String**| Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses &#x60;accountId&#x60;). Required for single-event operations.  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**CalendarOperationResult**](CalendarOperationResult.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getCalendarCapabilities"></a>
# **getCalendarCapabilities**
> CalendarCapabilitiesResponse getCalendarCapabilities(accountId)

Per-account capability flags.

Returns the capabilities the provider declares for the given connected account. The renderer uses these to enable/disable form fields (recurrence picker, attendee inputs, etc.). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses `accountId`). Required for single-event operations. 
try {
    val result : CalendarCapabilitiesResponse = apiInstance.getCalendarCapabilities(accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#getCalendarCapabilities")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#getCalendarCapabilities")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**| Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses &#x60;accountId&#x60;). Required for single-event operations.  | |

### Return type

[**CalendarCapabilitiesResponse**](CalendarCapabilitiesResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getCalendarEvent"></a>
# **getCalendarEvent**
> SpatioEvent getCalendarEvent(id, accountId, xWorkspaceID)

Fetch one event.

Requires &#x60;?account_id&#x3D;&#x60; to identify the source account. Response is the bare &#x60;Event&#x60; (not wrapped in CalendarOperationResult — distinct from the list/create/update shapes). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val id : kotlin.String = id_example // kotlin.String | Event id.
val accountId : kotlin.String = accountId_example // kotlin.String | Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses `accountId`). Required for single-event operations. 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
try {
    val result : SpatioEvent = apiInstance.getCalendarEvent(id, accountId, xWorkspaceID)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#getCalendarEvent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#getCalendarEvent")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Event id. | |
| **accountId** | **kotlin.String**| Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses &#x60;accountId&#x60;). Required for single-event operations.  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |

### Return type

[**SpatioEvent**](SpatioEvent.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listCalendarEvents"></a>
# **listCalendarEvents**
> ListCalendarEvents200Response listCalendarEvents(accountIds, providers, xWorkspaceID, timeMin, timeMax, limit)

List calendar events across connected accounts.

Fan-out list. Returns events across every connected calendar provider unless filtered by &#x60;account_ids[]&#x60; or &#x60;providers[]&#x60;. Supports the cross-platform repeated-or-comma-separated filter syntax (&#x60;?account_ids&#x3D;a&amp;account_ids&#x3D;b&#x60; or &#x60;?account_ids&#x3D;a,b&#x60;).  Time bounds (&#x60;timeMin&#x60; / &#x60;timeMax&#x60;) accept both RFC3339 and RFC3339Nano. The handler also accepts the snake_case &#x60;time_min&#x60; / &#x60;time_max&#x60; for direct curl callers; the spec models the camelCase form because that&#39;s what the renderer and SDKs use. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val accountIds : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to specific connected accounts.
val providers : kotlin.collections.List<kotlin.String> =  // kotlin.collections.List<kotlin.String> | Repeatable. Restrict to provider ids (`google-calendar`, etc.).
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val timeMin : java.time.OffsetDateTime = 2013-10-20T19:20:30+01:00 // java.time.OffsetDateTime | Inclusive lower-bound time. RFC3339 or RFC3339Nano.
val timeMax : java.time.OffsetDateTime = 2013-10-20T19:20:30+01:00 // java.time.OffsetDateTime | Inclusive upper-bound time.
val limit : kotlin.Int = 56 // kotlin.Int | Max events to return per page (default 50).
try {
    val result : ListCalendarEvents200Response = apiInstance.listCalendarEvents(accountIds, providers, xWorkspaceID, timeMin, timeMax, limit)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#listCalendarEvents")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#listCalendarEvents")
    e.printStackTrace()
}
```

### Parameters
| **accountIds** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to specific connected accounts. | [optional] |
| **providers** | [**kotlin.collections.List&lt;kotlin.String&gt;**](kotlin.String.md)| Repeatable. Restrict to provider ids (&#x60;google-calendar&#x60;, etc.). | [optional] |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| **timeMin** | **java.time.OffsetDateTime**| Inclusive lower-bound time. RFC3339 or RFC3339Nano. | [optional] |
| **timeMax** | **java.time.OffsetDateTime**| Inclusive upper-bound time. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **kotlin.Int**| Max events to return per page (default 50). | [optional] [default to 50] |

### Return type

[**ListCalendarEvents200Response**](ListCalendarEvents200Response.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listCalendarProviders"></a>
# **listCalendarProviders**
> CalendarProvidersInfo listCalendarProviders()

List supported calendar providers.

Static list of provider ids the Calendar platform can connect to. Returned regardless of which providers the caller has actually authorized. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
try {
    val result : CalendarProvidersInfo = apiInstance.listCalendarProviders()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#listCalendarProviders")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#listCalendarProviders")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**CalendarProvidersInfo**](CalendarProvidersInfo.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="syncCalendar"></a>
# **syncCalendar**
> CalendarSyncResponse syncCalendar(wait)

Trigger a sync across connected calendar accounts.

Enqueues sync jobs (one per connected calendar account) and returns immediately with the job ids. Pass &#x60;?wait&#x3D;true&#x60; to block until all jobs complete (10-second polling budget); the response is then &#x60;200&#x60; with &#x60;waited: true&#x60; and a &#x60;timed_out&#x60; flag if any job didn&#39;t finish in time. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val wait : kotlin.Boolean = true // kotlin.Boolean | Block until all sync jobs finish (10s timeout).
try {
    val result : CalendarSyncResponse = apiInstance.syncCalendar(wait)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#syncCalendar")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#syncCalendar")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **wait** | **kotlin.Boolean**| Block until all sync jobs finish (10s timeout). | [optional] [default to false] |

### Return type

[**CalendarSyncResponse**](CalendarSyncResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateCalendarEvent"></a>
# **updateCalendarEvent**
> CreateCalendarEvent201Response updateCalendarEvent(id, updateEventRequest, xWorkspaceID, accountId)

Update an event (sparse).

Partial update. &#x60;account_id&#x60; may be supplied in the body (preferred) or as &#x60;?account_id&#x3D;&#x60; query param — the renderer&#39;s update path puts it in the URL while create puts it in the body. &#x60;updates&#x60; is a free-form map; the platform&#39;s capability gate rejects fields the provider doesn&#39;t support. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val id : kotlin.String = id_example // kotlin.String | Event id.
val updateEventRequest : UpdateEventRequest =  // UpdateEventRequest | 
val xWorkspaceID : kotlin.String = xWorkspaceID_example // kotlin.String | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly. 
val accountId : kotlin.String = accountId_example // kotlin.String | Optional account-id filter (snake_case).
try {
    val result : CreateCalendarEvent201Response = apiInstance.updateCalendarEvent(id, updateEventRequest, xWorkspaceID, accountId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#updateCalendarEvent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#updateCalendarEvent")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**| Event id. | |
| **updateEventRequest** | [**UpdateEventRequest**](UpdateEventRequest.md)|  | |
| **xWorkspaceID** | **kotlin.String**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String**| Optional account-id filter (snake_case). | [optional] |

### Return type

[**CreateCalendarEvent201Response**](CreateCalendarEvent201Response.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceCreateCalendarEvent"></a>
# **workspaceCreateCalendarEvent**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateCalendarEvent(org, workspace, requestBody)

Workspace-scoped create-event (RBAC-protected).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateCalendarEvent(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#workspaceCreateCalendarEvent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#workspaceCreateCalendarEvent")
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

<a id="workspaceDeleteCalendarEvent"></a>
# **workspaceDeleteCalendarEvent**
> workspaceDeleteCalendarEvent(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.workspaceDeleteCalendarEvent(org, workspace, id)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#workspaceDeleteCalendarEvent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#workspaceDeleteCalendarEvent")
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

<a id="workspaceGetCalendarEvent"></a>
# **workspaceGetCalendarEvent**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetCalendarEvent(org, workspace, id)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetCalendarEvent(org, workspace, id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#workspaceGetCalendarEvent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#workspaceGetCalendarEvent")
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

<a id="workspaceListCalendarEvents"></a>
# **workspaceListCalendarEvents**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListCalendarEvents(org, workspace)

Workspace-scoped list-events (RBAC-protected).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListCalendarEvents(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#workspaceListCalendarEvents")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#workspaceListCalendarEvents")
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

<a id="workspaceListCalendarProviders"></a>
# **workspaceListCalendarProviders**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListCalendarProviders(org, workspace)

Workspace-scoped calendar providers.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListCalendarProviders(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#workspaceListCalendarProviders")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#workspaceListCalendarProviders")
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

<a id="workspaceUpdateCalendarEvent"></a>
# **workspaceUpdateCalendarEvent**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceUpdateCalendarEvent(org, workspace, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = CalendarApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceUpdateCalendarEvent(org, workspace, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CalendarApi#workspaceUpdateCalendarEvent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CalendarApi#workspaceUpdateCalendarEvent")
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

