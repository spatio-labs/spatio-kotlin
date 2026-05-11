# OAuthApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getJWKS**](OAuthApi.md#getJWKS) | **GET** /.well-known/jwks.json | JSON Web Key Set for id_token verification (RFC 7517). |
| [**getOAuthDiscovery**](OAuthApi.md#getOAuthDiscovery) | **GET** /.well-known/oauth-authorization-server | OAuth 2.1 authorization server metadata (RFC 8414). |
| [**getOpenIDConfiguration**](OAuthApi.md#getOpenIDConfiguration) | **GET** /.well-known/openid-configuration | OpenID Connect Discovery 1.0 metadata. |
| [**getUserInfo**](OAuthApi.md#getUserInfo) | **GET** /oauth2/userinfo | OIDC UserInfo (OpenID Connect Core 1.0 §5.3). |
| [**oauthAuthorize**](OAuthApi.md#oauthAuthorize) | **GET** /oauth2/authorize | OAuth 2.1 authorization endpoint (RFC 6749 + 7636 PKCE). |
| [**oauthIntrospect**](OAuthApi.md#oauthIntrospect) | **POST** /oauth2/introspect | RFC 7662 token introspection. Accepts both OAuth access tokens and PATs. |
| [**oauthRevoke**](OAuthApi.md#oauthRevoke) | **POST** /oauth2/revoke | RFC 7009 token revocation. Idempotent. |
| [**oauthToken**](OAuthApi.md#oauthToken) | **POST** /oauth2/token | Exchange authorization code or refresh token for an access token (+ id_token if &#x60;openid&#x60; scope). |
| [**postUserInfo**](OAuthApi.md#postUserInfo) | **POST** /oauth2/userinfo | Same as GET /oauth2/userinfo. Provided for clients that send the bearer in the body. |
| [**registerOAuthClient**](OAuthApi.md#registerOAuthClient) | **POST** /oauth2/register | Register a new OAuth 2.1 client (RFC 7591 dynamic client registration). |


<a id="getJWKS"></a>
# **getJWKS**
> JWKS getJWKS()

JSON Web Key Set for id_token verification (RFC 7517).

The set of public keys RPs use to verify Spatio-issued id_tokens. Cached for 5 minutes at the edge. Always includes the currently-active signing key plus any retired keys that may still be in circulation (id_token TTL is 1 hour + slack). 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OAuthApi()
try {
    val result : JWKS = apiInstance.getJWKS()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OAuthApi#getJWKS")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OAuthApi#getJWKS")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**JWKS**](JWKS.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getOAuthDiscovery"></a>
# **getOAuthDiscovery**
> DiscoveryDocument getOAuthDiscovery()

OAuth 2.1 authorization server metadata (RFC 8414).

Returns the canonical metadata for the Spatio OAuth 2.1 + OpenID Connect server. Third-party RPs use this to auto-discover endpoint URLs, supported scopes, and signing algorithms.  Identical payload to &#x60;/.well-known/openid-configuration&#x60; — either path is acceptable; OIDC clients prefer the openid-configuration alias. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OAuthApi()
try {
    val result : DiscoveryDocument = apiInstance.getOAuthDiscovery()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OAuthApi#getOAuthDiscovery")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OAuthApi#getOAuthDiscovery")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**DiscoveryDocument**](DiscoveryDocument.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getOpenIDConfiguration"></a>
# **getOpenIDConfiguration**
> DiscoveryDocument getOpenIDConfiguration()

OpenID Connect Discovery 1.0 metadata.

Alias of &#x60;/.well-known/oauth-authorization-server&#x60;. Provided so OIDC client libraries (NextAuth, Auth.js, oidc-client-ts, passport-openidconnect) auto-detect Spatio as an OIDC provider via their &#x60;wellKnown&#x60; / &#x60;discoveryUrl&#x60; config field. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OAuthApi()
try {
    val result : DiscoveryDocument = apiInstance.getOpenIDConfiguration()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OAuthApi#getOpenIDConfiguration")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OAuthApi#getOpenIDConfiguration")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**DiscoveryDocument**](DiscoveryDocument.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getUserInfo"></a>
# **getUserInfo**
> UserInfoResponse getUserInfo()

OIDC UserInfo (OpenID Connect Core 1.0 §5.3).

Returns user claims gated by the scopes on the presenting access token. &#x60;sub&#x60; is always returned; &#x60;email&#x60;, &#x60;name&#x60;, etc. require their respective scopes. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OAuthApi()
try {
    val result : UserInfoResponse = apiInstance.getUserInfo()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OAuthApi#getUserInfo")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OAuthApi#getUserInfo")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**UserInfoResponse**](UserInfoResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="oauthAuthorize"></a>
# **oauthAuthorize**
> oauthAuthorize(clientId, redirectUri, responseType, codeChallenge, codeChallengeMethod, scope, state, nonce, prompt, maxAge)

OAuth 2.1 authorization endpoint (RFC 6749 + 7636 PKCE).

Browser-redirect endpoint. Validates the client + redirect_uri, packs the request into a signed JWT, and 302s the user&#39;s browser to the consent UI. The consent UI then POSTs to &#x60;/oauth2/authorize/confirm&#x60; with the user&#39;s decision.  OIDC additions: &#x60;scope&#x3D;openid+profile+email&#x60;, &#x60;nonce&#x60;, &#x60;prompt&#x60; (none|login|consent), &#x60;max_age&#x60;. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OAuthApi()
val clientId : kotlin.String = clientId_example // kotlin.String | 
val redirectUri : java.net.URI = redirectUri_example // java.net.URI | 
val responseType : kotlin.String = responseType_example // kotlin.String | 
val codeChallenge : kotlin.String = codeChallenge_example // kotlin.String | 
val codeChallengeMethod : kotlin.String = codeChallengeMethod_example // kotlin.String | 
val scope : kotlin.String = scope_example // kotlin.String | 
val state : kotlin.String = state_example // kotlin.String | 
val nonce : kotlin.String = nonce_example // kotlin.String | 
val prompt : kotlin.String = prompt_example // kotlin.String | 
val maxAge : kotlin.Int = 56 // kotlin.Int | 
try {
    apiInstance.oauthAuthorize(clientId, redirectUri, responseType, codeChallenge, codeChallengeMethod, scope, state, nonce, prompt, maxAge)
} catch (e: ClientException) {
    println("4xx response calling OAuthApi#oauthAuthorize")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OAuthApi#oauthAuthorize")
    e.printStackTrace()
}
```

### Parameters
| **clientId** | **kotlin.String**|  | |
| **redirectUri** | **java.net.URI**|  | |
| **responseType** | **kotlin.String**|  | [enum: code] |
| **codeChallenge** | **kotlin.String**|  | |
| **codeChallengeMethod** | **kotlin.String**|  | [enum: S256] |
| **scope** | **kotlin.String**|  | [optional] |
| **state** | **kotlin.String**|  | [optional] |
| **nonce** | **kotlin.String**|  | [optional] |
| **prompt** | **kotlin.String**|  | [optional] [enum: none, login, consent] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **maxAge** | **kotlin.Int**|  | [optional] |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a id="oauthIntrospect"></a>
# **oauthIntrospect**
> IntrospectionResponse oauthIntrospect(token)

RFC 7662 token introspection. Accepts both OAuth access tokens and PATs.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OAuthApi()
val token : kotlin.String = token_example // kotlin.String | 
try {
    val result : IntrospectionResponse = apiInstance.oauthIntrospect(token)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OAuthApi#oauthIntrospect")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OAuthApi#oauthIntrospect")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **token** | **kotlin.String**|  | |

### Return type

[**IntrospectionResponse**](IntrospectionResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a id="oauthRevoke"></a>
# **oauthRevoke**
> oauthRevoke(token)

RFC 7009 token revocation. Idempotent.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OAuthApi()
val token : kotlin.String = token_example // kotlin.String | 
try {
    apiInstance.oauthRevoke(token)
} catch (e: ClientException) {
    println("4xx response calling OAuthApi#oauthRevoke")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OAuthApi#oauthRevoke")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **token** | **kotlin.String**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: Not defined

<a id="oauthToken"></a>
# **oauthToken**
> TokenResponse oauthToken(grantType, code, codeVerifier, redirectUri, refreshToken, clientId, clientSecret)

Exchange authorization code or refresh token for an access token (+ id_token if &#x60;openid&#x60; scope).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OAuthApi()
val grantType : kotlin.String = grantType_example // kotlin.String | 
val code : kotlin.String = code_example // kotlin.String | Required for authorization_code grant.
val codeVerifier : kotlin.String = codeVerifier_example // kotlin.String | PKCE verifier — required for authorization_code grant.
val redirectUri : java.net.URI = redirectUri_example // java.net.URI | 
val refreshToken : kotlin.String = refreshToken_example // kotlin.String | Required for refresh_token grant.
val clientId : kotlin.String = clientId_example // kotlin.String | 
val clientSecret : kotlin.String = clientSecret_example // kotlin.String | 
try {
    val result : TokenResponse = apiInstance.oauthToken(grantType, code, codeVerifier, redirectUri, refreshToken, clientId, clientSecret)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OAuthApi#oauthToken")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OAuthApi#oauthToken")
    e.printStackTrace()
}
```

### Parameters
| **grantType** | **kotlin.String**|  | [enum: authorization_code, refresh_token] |
| **code** | **kotlin.String**| Required for authorization_code grant. | [optional] |
| **codeVerifier** | **kotlin.String**| PKCE verifier — required for authorization_code grant. | [optional] |
| **redirectUri** | **java.net.URI**|  | [optional] |
| **refreshToken** | **kotlin.String**| Required for refresh_token grant. | [optional] |
| **clientId** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **clientSecret** | **kotlin.String**|  | [optional] |

### Return type

[**TokenResponse**](TokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a id="postUserInfo"></a>
# **postUserInfo**
> UserInfoResponse postUserInfo()

Same as GET /oauth2/userinfo. Provided for clients that send the bearer in the body.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OAuthApi()
try {
    val result : UserInfoResponse = apiInstance.postUserInfo()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OAuthApi#postUserInfo")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OAuthApi#postUserInfo")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**UserInfoResponse**](UserInfoResponse.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="registerOAuthClient"></a>
# **registerOAuthClient**
> ClientRegistrationResponse registerOAuthClient(clientRegistrationRequest)

Register a new OAuth 2.1 client (RFC 7591 dynamic client registration).

Returns a fresh &#x60;client_id&#x60; (and, for confidential clients, &#x60;client_secret&#x60;) plus a one-time &#x60;registration_access_token&#x60; the client can use later to update its registration. Public clients (mobile, SPA) MUST use &#x60;token_endpoint_auth_method: none&#x60; and PKCE.  Rate-limited to 10 registrations per hour per source IP. 

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = OAuthApi()
val clientRegistrationRequest : ClientRegistrationRequest =  // ClientRegistrationRequest | 
try {
    val result : ClientRegistrationResponse = apiInstance.registerOAuthClient(clientRegistrationRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OAuthApi#registerOAuthClient")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OAuthApi#registerOAuthClient")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **clientRegistrationRequest** | [**ClientRegistrationRequest**](ClientRegistrationRequest.md)|  | |

### Return type

[**ClientRegistrationResponse**](ClientRegistrationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

