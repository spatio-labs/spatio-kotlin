# OrganizationsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**acceptOrganizationInvitation**](OrganizationsApi.md#acceptOrganizationInvitation) | **POST** /v1/organizations/{org}/accept-invitation | Accept an invitation to this organization. |
| [**addOrganizationMember**](OrganizationsApi.md#addOrganizationMember) | **POST** /v1/organizations/{org}/members | Add a member directly (skips invitation flow). |
| [**createOrganization**](OrganizationsApi.md#createOrganization) | **POST** /v1/organizations | Create an organization. |
| [**createOrganizationConcept**](OrganizationsApi.md#createOrganizationConcept) | **POST** /v1/organizations/{org}/concepts | Create an org-brain concept (admin+ only). |
| [**createOrganizationCustomRole**](OrganizationsApi.md#createOrganizationCustomRole) | **POST** /v1/organizations/{org}/roles | Create a custom role (admin+ only). |
| [**createOrganizationInvitation**](OrganizationsApi.md#createOrganizationInvitation) | **POST** /v1/organizations/{org}/invitations | Invite a user to the organization. |
| [**createOrganizationWorkspace**](OrganizationsApi.md#createOrganizationWorkspace) | **POST** /v1/organizations/{org}/workspaces | Create a workspace inside an organization. |
| [**deleteOrganization**](OrganizationsApi.md#deleteOrganization) | **DELETE** /v1/organizations/{org} | Delete an organization. |
| [**deleteOrganizationConcept**](OrganizationsApi.md#deleteOrganizationConcept) | **DELETE** /v1/organizations/{org}/concepts/{slug} | Delete a concept (admin+ only). |
| [**deleteOrganizationCustomRole**](OrganizationsApi.md#deleteOrganizationCustomRole) | **DELETE** /v1/organizations/{org}/roles/{roleId} | Delete a custom role (admin+ only). |
| [**deleteOrganizationLogo**](OrganizationsApi.md#deleteOrganizationLogo) | **DELETE** /v1/organizations/{org}/logo | Delete the organization logo. |
| [**getOrganization**](OrganizationsApi.md#getOrganization) | **GET** /v1/organizations/{org} | Fetch a single organization. |
| [**getOrganizationConcept**](OrganizationsApi.md#getOrganizationConcept) | **GET** /v1/organizations/{org}/concepts/{slug} | Fetch a concept. |
| [**listMyOrganizations**](OrganizationsApi.md#listMyOrganizations) | **GET** /v1/organizations | List the caller&#39;s organizations. |
| [**listOrganizationAuditLog**](OrganizationsApi.md#listOrganizationAuditLog) | **GET** /v1/organizations/{org}/audit-log | Read the organization audit log (admin / billing-admin only). |
| [**listOrganizationConcepts**](OrganizationsApi.md#listOrganizationConcepts) | **GET** /v1/organizations/{org}/concepts | List org-brain concepts (curated knowledge surfaced to agents). |
| [**listOrganizationCustomRoles**](OrganizationsApi.md#listOrganizationCustomRoles) | **GET** /v1/organizations/{org}/roles | List custom roles defined on the organization. |
| [**listOrganizationInvitations**](OrganizationsApi.md#listOrganizationInvitations) | **GET** /v1/organizations/{org}/invitations | List pending invitations for an organization. |
| [**listOrganizationMembers**](OrganizationsApi.md#listOrganizationMembers) | **GET** /v1/organizations/{org}/members | List members of an organization. |
| [**listOrganizationWorkspaces**](OrganizationsApi.md#listOrganizationWorkspaces) | **GET** /v1/organizations/{org}/workspaces | List workspaces in an organization. |
| [**removeOrganizationMember**](OrganizationsApi.md#removeOrganizationMember) | **DELETE** /v1/organizations/{org}/members/{memberId} | Remove a member from the organization. |
| [**resendOrganizationInvitation**](OrganizationsApi.md#resendOrganizationInvitation) | **POST** /v1/organizations/{org}/invitations/{invitationId}/resend | Revoke and reissue an invitation with a fresh token. |
| [**revokeOrganizationInvitation**](OrganizationsApi.md#revokeOrganizationInvitation) | **DELETE** /v1/organizations/{org}/invitations/{invitationId} | Revoke a pending invitation. |
| [**updateOrganization**](OrganizationsApi.md#updateOrganization) | **PATCH** /v1/organizations/{org} | Update organization metadata. |
| [**updateOrganizationConcept**](OrganizationsApi.md#updateOrganizationConcept) | **PATCH** /v1/organizations/{org}/concepts/{slug} | Update a concept (admin+ only). |
| [**updateOrganizationCustomRole**](OrganizationsApi.md#updateOrganizationCustomRole) | **PATCH** /v1/organizations/{org}/roles/{roleId} | Update a custom role (admin+ only). |
| [**updateOrganizationMember**](OrganizationsApi.md#updateOrganizationMember) | **PATCH** /v1/organizations/{org}/members/{memberId} | Update a member&#39;s role. |
| [**uploadOrganizationLogo**](OrganizationsApi.md#uploadOrganizationLogo) | **POST** /v1/organizations/{org}/logo | Upload (or replace) the organization logo. Multipart. |


<a id="acceptOrganizationInvitation"></a>
# **acceptOrganizationInvitation**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; acceptOrganizationInvitation(org, acceptOrganizationInvitationRequest)

Accept an invitation to this organization.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val acceptOrganizationInvitationRequest : AcceptOrganizationInvitationRequest =  // AcceptOrganizationInvitationRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.acceptOrganizationInvitation(org, acceptOrganizationInvitationRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#acceptOrganizationInvitation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#acceptOrganizationInvitation")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **acceptOrganizationInvitationRequest** | [**AcceptOrganizationInvitationRequest**](AcceptOrganizationInvitationRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="addOrganizationMember"></a>
# **addOrganizationMember**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; addOrganizationMember(org, addOrganizationMemberRequest)

Add a member directly (skips invitation flow).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val addOrganizationMemberRequest : AddOrganizationMemberRequest =  // AddOrganizationMemberRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.addOrganizationMember(org, addOrganizationMemberRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#addOrganizationMember")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#addOrganizationMember")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **addOrganizationMemberRequest** | [**AddOrganizationMemberRequest**](AddOrganizationMemberRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createOrganization"></a>
# **createOrganization**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; createOrganization(createOrganizationRequest)

Create an organization.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val createOrganizationRequest : CreateOrganizationRequest =  // CreateOrganizationRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.createOrganization(createOrganizationRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#createOrganization")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#createOrganization")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createOrganizationRequest** | [**CreateOrganizationRequest**](CreateOrganizationRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createOrganizationConcept"></a>
# **createOrganizationConcept**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; createOrganizationConcept(org, requestBody)

Create an org-brain concept (admin+ only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.createOrganizationConcept(org, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#createOrganizationConcept")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#createOrganizationConcept")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
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

<a id="createOrganizationCustomRole"></a>
# **createOrganizationCustomRole**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; createOrganizationCustomRole(org, requestBody)

Create a custom role (admin+ only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.createOrganizationCustomRole(org, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#createOrganizationCustomRole")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#createOrganizationCustomRole")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
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

<a id="createOrganizationInvitation"></a>
# **createOrganizationInvitation**
> OrganizationInvitation createOrganizationInvitation(org, createOrganizationInvitationRequest)

Invite a user to the organization.

Pending invitations count toward seat cap. Free-tier callers at the cap receive a &#x60;402&#x60; with billing-upgrade payload; paid-tier auto-scales the Stripe quantity. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val createOrganizationInvitationRequest : CreateOrganizationInvitationRequest =  // CreateOrganizationInvitationRequest | 
try {
    val result : OrganizationInvitation = apiInstance.createOrganizationInvitation(org, createOrganizationInvitationRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#createOrganizationInvitation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#createOrganizationInvitation")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createOrganizationInvitationRequest** | [**CreateOrganizationInvitationRequest**](CreateOrganizationInvitationRequest.md)|  | |

### Return type

[**OrganizationInvitation**](OrganizationInvitation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createOrganizationWorkspace"></a>
# **createOrganizationWorkspace**
> WorkspaceEnvelope createOrganizationWorkspace(org, createWorkspaceRequest)

Create a workspace inside an organization.

Requires the &#x60;OrgActionCreateWorkspace&#x60; action permission. Slug collisions auto-suffix (&#x60;-2&#x60;, &#x60;-3&#x60;, ...). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val createWorkspaceRequest : CreateWorkspaceRequest =  // CreateWorkspaceRequest | 
try {
    val result : WorkspaceEnvelope = apiInstance.createOrganizationWorkspace(org, createWorkspaceRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#createOrganizationWorkspace")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#createOrganizationWorkspace")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createWorkspaceRequest** | [**CreateWorkspaceRequest**](CreateWorkspaceRequest.md)|  | |

### Return type

[**WorkspaceEnvelope**](WorkspaceEnvelope.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteOrganization"></a>
# **deleteOrganization**
> deleteOrganization(org)

Delete an organization.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | Organization id or slug.
try {
    apiInstance.deleteOrganization(org)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#deleteOrganization")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#deleteOrganization")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org** | **kotlin.String**| Organization id or slug. | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="deleteOrganizationConcept"></a>
# **deleteOrganizationConcept**
> deleteOrganizationConcept(org, slug)

Delete a concept (admin+ only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val slug : kotlin.String = slug_example // kotlin.String | 
try {
    apiInstance.deleteOrganizationConcept(org, slug)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#deleteOrganizationConcept")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#deleteOrganizationConcept")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **slug** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="deleteOrganizationCustomRole"></a>
# **deleteOrganizationCustomRole**
> deleteOrganizationCustomRole(org, roleId)

Delete a custom role (admin+ only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val roleId : kotlin.String = roleId_example // kotlin.String | 
try {
    apiInstance.deleteOrganizationCustomRole(org, roleId)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#deleteOrganizationCustomRole")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#deleteOrganizationCustomRole")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **roleId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="deleteOrganizationLogo"></a>
# **deleteOrganizationLogo**
> deleteOrganizationLogo(org)

Delete the organization logo.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
try {
    apiInstance.deleteOrganizationLogo(org)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#deleteOrganizationLogo")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#deleteOrganizationLogo")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getOrganization"></a>
# **getOrganization**
> OrganizationDetailLegacy getOrganization(org)

Fetch a single organization.

**Wire format note:** response uses PascalCase keys (&#x60;ID&#x60;, &#x60;Name&#x60;, &#x60;Slug&#x60;, ...) — distinct from the rest of the SpatioAPI&#39;s camelCase convention. Documented as-is; a future cleanup will harmonize. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | Organization id or slug.
try {
    val result : OrganizationDetailLegacy = apiInstance.getOrganization(org)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#getOrganization")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#getOrganization")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org** | **kotlin.String**| Organization id or slug. | |

### Return type

[**OrganizationDetailLegacy**](OrganizationDetailLegacy.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getOrganizationConcept"></a>
# **getOrganizationConcept**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getOrganizationConcept(org, slug)

Fetch a concept.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val slug : kotlin.String = slug_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getOrganizationConcept(org, slug)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#getOrganizationConcept")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#getOrganizationConcept")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **slug** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listMyOrganizations"></a>
# **listMyOrganizations**
> OrganizationListResponse listMyOrganizations()

List the caller&#39;s organizations.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
try {
    val result : OrganizationListResponse = apiInstance.listMyOrganizations()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#listMyOrganizations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#listMyOrganizations")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**OrganizationListResponse**](OrganizationListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listOrganizationAuditLog"></a>
# **listOrganizationAuditLog**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listOrganizationAuditLog(org, limit, cursor)

Read the organization audit log (admin / billing-admin only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val limit : kotlin.Int = 56 // kotlin.Int | 
val cursor : kotlin.String = cursor_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listOrganizationAuditLog(org, limit, cursor)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#listOrganizationAuditLog")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#listOrganizationAuditLog")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **limit** | **kotlin.Int**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cursor** | **kotlin.String**|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listOrganizationConcepts"></a>
# **listOrganizationConcepts**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listOrganizationConcepts(org)

List org-brain concepts (curated knowledge surfaced to agents).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listOrganizationConcepts(org)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#listOrganizationConcepts")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#listOrganizationConcepts")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listOrganizationCustomRoles"></a>
# **listOrganizationCustomRoles**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listOrganizationCustomRoles(org)

List custom roles defined on the organization.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listOrganizationCustomRoles(org)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#listOrganizationCustomRoles")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#listOrganizationCustomRoles")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listOrganizationInvitations"></a>
# **listOrganizationInvitations**
> OrganizationInvitationListResponse listOrganizationInvitations(org)

List pending invitations for an organization.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
try {
    val result : OrganizationInvitationListResponse = apiInstance.listOrganizationInvitations(org)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#listOrganizationInvitations")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#listOrganizationInvitations")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org** | **kotlin.String**|  | |

### Return type

[**OrganizationInvitationListResponse**](OrganizationInvitationListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listOrganizationMembers"></a>
# **listOrganizationMembers**
> OrganizationMemberListResponse listOrganizationMembers(org)

List members of an organization.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
try {
    val result : OrganizationMemberListResponse = apiInstance.listOrganizationMembers(org)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#listOrganizationMembers")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#listOrganizationMembers")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org** | **kotlin.String**|  | |

### Return type

[**OrganizationMemberListResponse**](OrganizationMemberListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listOrganizationWorkspaces"></a>
# **listOrganizationWorkspaces**
> WorkspaceListResponse listOrganizationWorkspaces(org)

List workspaces in an organization.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
try {
    val result : WorkspaceListResponse = apiInstance.listOrganizationWorkspaces(org)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#listOrganizationWorkspaces")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#listOrganizationWorkspaces")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org** | **kotlin.String**|  | |

### Return type

[**WorkspaceListResponse**](WorkspaceListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="removeOrganizationMember"></a>
# **removeOrganizationMember**
> removeOrganizationMember(org, memberId)

Remove a member from the organization.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val memberId : kotlin.String = memberId_example // kotlin.String | 
try {
    apiInstance.removeOrganizationMember(org, memberId)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#removeOrganizationMember")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#removeOrganizationMember")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **memberId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="resendOrganizationInvitation"></a>
# **resendOrganizationInvitation**
> OrganizationInvitation resendOrganizationInvitation(org, invitationId)

Revoke and reissue an invitation with a fresh token.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val invitationId : kotlin.String = invitationId_example // kotlin.String | 
try {
    val result : OrganizationInvitation = apiInstance.resendOrganizationInvitation(org, invitationId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#resendOrganizationInvitation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#resendOrganizationInvitation")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invitationId** | **kotlin.String**|  | |

### Return type

[**OrganizationInvitation**](OrganizationInvitation.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="revokeOrganizationInvitation"></a>
# **revokeOrganizationInvitation**
> revokeOrganizationInvitation(org, invitationId)

Revoke a pending invitation.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val invitationId : kotlin.String = invitationId_example // kotlin.String | 
try {
    apiInstance.revokeOrganizationInvitation(org, invitationId)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#revokeOrganizationInvitation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#revokeOrganizationInvitation")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invitationId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateOrganization"></a>
# **updateOrganization**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateOrganization(org, updateOrganizationRequest)

Update organization metadata.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | Organization id or slug.
val updateOrganizationRequest : UpdateOrganizationRequest =  // UpdateOrganizationRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateOrganization(org, updateOrganizationRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#updateOrganization")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#updateOrganization")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**| Organization id or slug. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateOrganizationRequest** | [**UpdateOrganizationRequest**](UpdateOrganizationRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateOrganizationConcept"></a>
# **updateOrganizationConcept**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateOrganizationConcept(org, slug, requestBody)

Update a concept (admin+ only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val slug : kotlin.String = slug_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateOrganizationConcept(org, slug, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#updateOrganizationConcept")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#updateOrganizationConcept")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **slug** | **kotlin.String**|  | |
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

<a id="updateOrganizationCustomRole"></a>
# **updateOrganizationCustomRole**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateOrganizationCustomRole(org, roleId, requestBody)

Update a custom role (admin+ only).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val roleId : kotlin.String = roleId_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateOrganizationCustomRole(org, roleId, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#updateOrganizationCustomRole")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#updateOrganizationCustomRole")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **roleId** | **kotlin.String**|  | |
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

<a id="updateOrganizationMember"></a>
# **updateOrganizationMember**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; updateOrganizationMember(org, memberId, updateOrganizationMemberRequest)

Update a member&#39;s role.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val memberId : kotlin.String = memberId_example // kotlin.String | 
val updateOrganizationMemberRequest : UpdateOrganizationMemberRequest =  // UpdateOrganizationMemberRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.updateOrganizationMember(org, memberId, updateOrganizationMemberRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#updateOrganizationMember")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#updateOrganizationMember")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **memberId** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateOrganizationMemberRequest** | [**UpdateOrganizationMemberRequest**](UpdateOrganizationMemberRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="uploadOrganizationLogo"></a>
# **uploadOrganizationLogo**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; uploadOrganizationLogo(org, file)

Upload (or replace) the organization logo. Multipart.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OrganizationsApi()
val org : kotlin.String = org_example // kotlin.String | 
val file : java.io.File = BINARY_DATA_HERE // java.io.File | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.uploadOrganizationLogo(org, file)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OrganizationsApi#uploadOrganizationLogo")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OrganizationsApi#uploadOrganizationLogo")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
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

