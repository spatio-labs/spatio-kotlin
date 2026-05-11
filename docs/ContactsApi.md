# ContactsApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**assignContactCategory**](ContactsApi.md#assignContactCategory) | **POST** /v1/contacts/{id}/categories | Assign a category to a contact. |
| [**createContact**](ContactsApi.md#createContact) | **POST** /v1/contacts | Create a contact. |
| [**createContactCategory**](ContactsApi.md#createContactCategory) | **POST** /v1/contacts/categories | Create a contact category. |
| [**deleteContact**](ContactsApi.md#deleteContact) | **DELETE** /v1/contacts/{id} | Delete a contact. |
| [**deleteContactCategory**](ContactsApi.md#deleteContactCategory) | **DELETE** /v1/contacts/categories/{id} | Delete a category. |
| [**getContact**](ContactsApi.md#getContact) | **GET** /v1/contacts/{id} | Fetch a contact. |
| [**listContactCategories**](ContactsApi.md#listContactCategories) | **GET** /v1/contacts/categories | List contact categories. Requires &#x60;organization_id&#x60; query param. |
| [**listContactProviders**](ContactsApi.md#listContactProviders) | **GET** /v1/contacts/providers | List supported contact providers (native + OAuth-connected). |
| [**listContacts**](ContactsApi.md#listContacts) | **GET** /v1/contacts | List the caller&#39;s contacts (across providers). |
| [**unassignContactCategory**](ContactsApi.md#unassignContactCategory) | **DELETE** /v1/contacts/{id}/categories/{categoryId} | Remove a category from a contact. |
| [**updateContact**](ContactsApi.md#updateContact) | **PATCH** /v1/contacts/{id} | Update a contact. |
| [**updateContactCategory**](ContactsApi.md#updateContactCategory) | **PATCH** /v1/contacts/categories/{id} | Update a category. |


<a id="assignContactCategory"></a>
# **assignContactCategory**
> assignContactCategory(id, assignContactCategoryRequest)

Assign a category to a contact.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ContactsApi()
val id : kotlin.String = id_example // kotlin.String | 
val assignContactCategoryRequest : AssignContactCategoryRequest =  // AssignContactCategoryRequest | 
try {
    apiInstance.assignContactCategory(id, assignContactCategoryRequest)
} catch (e: ClientException) {
    println("4xx response calling ContactsApi#assignContactCategory")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ContactsApi#assignContactCategory")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **assignContactCategoryRequest** | [**AssignContactCategoryRequest**](AssignContactCategoryRequest.md)|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createContact"></a>
# **createContact**
> Contact createContact(createContactRequest)

Create a contact.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ContactsApi()
val createContactRequest : CreateContactRequest =  // CreateContactRequest | 
try {
    val result : Contact = apiInstance.createContact(createContactRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ContactsApi#createContact")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ContactsApi#createContact")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createContactRequest** | [**CreateContactRequest**](CreateContactRequest.md)|  | |

### Return type

[**Contact**](Contact.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="createContactCategory"></a>
# **createContactCategory**
> ContactCategory createContactCategory(createContactCategoryRequest)

Create a contact category.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ContactsApi()
val createContactCategoryRequest : CreateContactCategoryRequest =  // CreateContactCategoryRequest | 
try {
    val result : ContactCategory = apiInstance.createContactCategory(createContactCategoryRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ContactsApi#createContactCategory")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ContactsApi#createContactCategory")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createContactCategoryRequest** | [**CreateContactCategoryRequest**](CreateContactCategoryRequest.md)|  | |

### Return type

[**ContactCategory**](ContactCategory.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="deleteContact"></a>
# **deleteContact**
> deleteContact(id)

Delete a contact.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ContactsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteContact(id)
} catch (e: ClientException) {
    println("4xx response calling ContactsApi#deleteContact")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ContactsApi#deleteContact")
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

<a id="deleteContactCategory"></a>
# **deleteContactCategory**
> deleteContactCategory(id)

Delete a category.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ContactsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    apiInstance.deleteContactCategory(id)
} catch (e: ClientException) {
    println("4xx response calling ContactsApi#deleteContactCategory")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ContactsApi#deleteContactCategory")
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

<a id="getContact"></a>
# **getContact**
> Contact getContact(id)

Fetch a contact.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ContactsApi()
val id : kotlin.String = id_example // kotlin.String | 
try {
    val result : Contact = apiInstance.getContact(id)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ContactsApi#getContact")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ContactsApi#getContact")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **kotlin.String**|  | |

### Return type

[**Contact**](Contact.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listContactCategories"></a>
# **listContactCategories**
> ContactCategoryListResponse listContactCategories(organizationId)

List contact categories. Requires &#x60;organization_id&#x60; query param.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ContactsApi()
val organizationId : kotlin.String = organizationId_example // kotlin.String | 
try {
    val result : ContactCategoryListResponse = apiInstance.listContactCategories(organizationId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ContactsApi#listContactCategories")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ContactsApi#listContactCategories")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organizationId** | **kotlin.String**|  | |

### Return type

[**ContactCategoryListResponse**](ContactCategoryListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listContactProviders"></a>
# **listContactProviders**
> ContactProviderListResponse listContactProviders()

List supported contact providers (native + OAuth-connected).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ContactsApi()
try {
    val result : ContactProviderListResponse = apiInstance.listContactProviders()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ContactsApi#listContactProviders")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ContactsApi#listContactProviders")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ContactProviderListResponse**](ContactProviderListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listContacts"></a>
# **listContacts**
> ContactListResponse listContacts(limit, provider, search)

List the caller&#39;s contacts (across providers).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ContactsApi()
val limit : kotlin.Int = 56 // kotlin.Int | 
val provider : kotlin.String = provider_example // kotlin.String | 
val search : kotlin.String = search_example // kotlin.String | 
try {
    val result : ContactListResponse = apiInstance.listContacts(limit, provider, search)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ContactsApi#listContacts")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ContactsApi#listContacts")
    e.printStackTrace()
}
```

### Parameters
| **limit** | **kotlin.Int**|  | [optional] |
| **provider** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **search** | **kotlin.String**|  | [optional] |

### Return type

[**ContactListResponse**](ContactListResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="unassignContactCategory"></a>
# **unassignContactCategory**
> unassignContactCategory(id, categoryId)

Remove a category from a contact.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ContactsApi()
val id : kotlin.String = id_example // kotlin.String | 
val categoryId : kotlin.String = categoryId_example // kotlin.String | 
try {
    apiInstance.unassignContactCategory(id, categoryId)
} catch (e: ClientException) {
    println("4xx response calling ContactsApi#unassignContactCategory")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ContactsApi#unassignContactCategory")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **categoryId** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="updateContact"></a>
# **updateContact**
> Contact updateContact(id, updateContactRequest)

Update a contact.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ContactsApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateContactRequest : UpdateContactRequest =  // UpdateContactRequest | 
try {
    val result : Contact = apiInstance.updateContact(id, updateContactRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ContactsApi#updateContact")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ContactsApi#updateContact")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateContactRequest** | [**UpdateContactRequest**](UpdateContactRequest.md)|  | |

### Return type

[**Contact**](Contact.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="updateContactCategory"></a>
# **updateContactCategory**
> ContactCategory updateContactCategory(id, updateContactCategoryRequest)

Update a category.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = ContactsApi()
val id : kotlin.String = id_example // kotlin.String | 
val updateContactCategoryRequest : UpdateContactCategoryRequest =  // UpdateContactCategoryRequest | 
try {
    val result : ContactCategory = apiInstance.updateContactCategory(id, updateContactCategoryRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling ContactsApi#updateContactCategory")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling ContactsApi#updateContactCategory")
    e.printStackTrace()
}
```

### Parameters
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateContactCategoryRequest** | [**UpdateContactCategoryRequest**](UpdateContactCategoryRequest.md)|  | |

### Return type

[**ContactCategory**](ContactCategory.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

