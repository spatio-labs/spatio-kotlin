# RepoApi

All URIs are relative to *https://api.spatio.app*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createRepoBranch**](RepoApi.md#createRepoBranch) | **POST** /v1/repos/repositories/{owner}/{repo}/branches | Create a branch (from a base sha). |
| [**createRepoPullRequest**](RepoApi.md#createRepoPullRequest) | **POST** /v1/repos/repositories/{owner}/{repo}/pulls | Open a pull request. |
| [**createRepoRepository**](RepoApi.md#createRepoRepository) | **POST** /v1/repos/repositories | Create a repository. |
| [**getRepoCommit**](RepoApi.md#getRepoCommit) | **GET** /v1/repos/repositories/{owner}/{repo}/commits/{sha} | Fetch a single commit. |
| [**getRepoRepository**](RepoApi.md#getRepoRepository) | **GET** /v1/repos/repositories/{owner}/{repo} | Fetch a single repository. |
| [**linkRepoTask**](RepoApi.md#linkRepoTask) | **POST** /v1/repos/repositories/{owner}/{repo}/tasks/link | Link an existing Spatio task to this repo, allocating a per-repo number. |
| [**listRepoBranches**](RepoApi.md#listRepoBranches) | **GET** /v1/repos/repositories/{owner}/{repo}/branches | List branches on a repository. |
| [**listRepoCommits**](RepoApi.md#listRepoCommits) | **GET** /v1/repos/repositories/{owner}/{repo}/commits | List commits on a repository. |
| [**listRepoPullRequests**](RepoApi.md#listRepoPullRequests) | **GET** /v1/repos/repositories/{owner}/{repo}/pulls | List pull requests on a repository. |
| [**listRepoRepositories**](RepoApi.md#listRepoRepositories) | **GET** /v1/repos/repositories | List the caller&#39;s accessible repositories. |
| [**listRepoTasks**](RepoApi.md#listRepoTasks) | **GET** /v1/repos/repositories/{owner}/{repo}/tasks | List tasks linked to this repo (the \&quot;issues\&quot; surface). |
| [**listRepoWorkflows**](RepoApi.md#listRepoWorkflows) | **GET** /v1/repos/repositories/{owner}/{repo}/workflows | List CI workflows. |
| [**mergeRepoPullRequest**](RepoApi.md#mergeRepoPullRequest) | **POST** /v1/repos/repositories/{owner}/{repo}/pulls/{number}/merge | Merge a pull request. |
| [**triggerRepoWorkflow**](RepoApi.md#triggerRepoWorkflow) | **POST** /v1/repos/repositories/{owner}/{repo}/workflows/{id}/trigger | Trigger a workflow_dispatch run. |
| [**workspaceCreateRepoBranch**](RepoApi.md#workspaceCreateRepoBranch) | **POST** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories/{owner}/{repo}/branches |  |
| [**workspaceCreateRepoPullRequest**](RepoApi.md#workspaceCreateRepoPullRequest) | **POST** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories/{owner}/{repo}/pulls |  |
| [**workspaceCreateRepoRepository**](RepoApi.md#workspaceCreateRepoRepository) | **POST** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories |  |
| [**workspaceGetRepoCommit**](RepoApi.md#workspaceGetRepoCommit) | **GET** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories/{owner}/{repo}/commits/{sha} |  |
| [**workspaceGetRepoRepository**](RepoApi.md#workspaceGetRepoRepository) | **GET** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories/{owner}/{repo} |  |
| [**workspaceLinkRepoTask**](RepoApi.md#workspaceLinkRepoTask) | **POST** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories/{owner}/{repo}/tasks/link |  |
| [**workspaceListRepoBranches**](RepoApi.md#workspaceListRepoBranches) | **GET** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories/{owner}/{repo}/branches |  |
| [**workspaceListRepoCommits**](RepoApi.md#workspaceListRepoCommits) | **GET** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories/{owner}/{repo}/commits |  |
| [**workspaceListRepoPullRequests**](RepoApi.md#workspaceListRepoPullRequests) | **GET** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories/{owner}/{repo}/pulls |  |
| [**workspaceListRepoRepositories**](RepoApi.md#workspaceListRepoRepositories) | **GET** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories |  |
| [**workspaceListRepoTasks**](RepoApi.md#workspaceListRepoTasks) | **GET** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories/{owner}/{repo}/tasks |  |
| [**workspaceListRepoWorkflows**](RepoApi.md#workspaceListRepoWorkflows) | **GET** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories/{owner}/{repo}/workflows |  |
| [**workspaceMergeRepoPullRequest**](RepoApi.md#workspaceMergeRepoPullRequest) | **POST** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories/{owner}/{repo}/pulls/{number}/merge |  |
| [**workspaceTriggerRepoWorkflow**](RepoApi.md#workspaceTriggerRepoWorkflow) | **POST** /v1/organizations/{org}/workspaces/{workspace}/repos/repositories/{owner}/{repo}/workflows/{id}/trigger |  |


<a id="createRepoBranch"></a>
# **createRepoBranch**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; createRepoBranch(owner, repo, requestBody)

Create a branch (from a base sha).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.createRepoBranch(owner, repo, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#createRepoBranch")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#createRepoBranch")
    e.printStackTrace()
}
```

### Parameters
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
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

<a id="createRepoPullRequest"></a>
# **createRepoPullRequest**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; createRepoPullRequest(owner, repo, requestBody)

Open a pull request.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.createRepoPullRequest(owner, repo, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#createRepoPullRequest")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#createRepoPullRequest")
    e.printStackTrace()
}
```

### Parameters
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
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

<a id="createRepoRepository"></a>
# **createRepoRepository**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; createRepoRepository(requestBody)

Create a repository.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.createRepoRepository(requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#createRepoRepository")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#createRepoRepository")
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

<a id="getRepoCommit"></a>
# **getRepoCommit**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getRepoCommit(owner, repo, sha)

Fetch a single commit.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val sha : kotlin.String = sha_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getRepoCommit(owner, repo, sha)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#getRepoCommit")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#getRepoCommit")
    e.printStackTrace()
}
```

### Parameters
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sha** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="getRepoRepository"></a>
# **getRepoRepository**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; getRepoRepository(owner, repo)

Fetch a single repository.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.getRepoRepository(owner, repo)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#getRepoRepository")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#getRepoRepository")
    e.printStackTrace()
}
```

### Parameters
| **owner** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **repo** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="linkRepoTask"></a>
# **linkRepoTask**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; linkRepoTask(owner, repo, linkRepoTaskRequest)

Link an existing Spatio task to this repo, allocating a per-repo number.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val linkRepoTaskRequest : LinkRepoTaskRequest =  // LinkRepoTaskRequest | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.linkRepoTask(owner, repo, linkRepoTaskRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#linkRepoTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#linkRepoTask")
    e.printStackTrace()
}
```

### Parameters
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **linkRepoTaskRequest** | [**LinkRepoTaskRequest**](LinkRepoTaskRequest.md)|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="listRepoBranches"></a>
# **listRepoBranches**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listRepoBranches(owner, repo)

List branches on a repository.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listRepoBranches(owner, repo)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#listRepoBranches")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#listRepoBranches")
    e.printStackTrace()
}
```

### Parameters
| **owner** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **repo** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listRepoCommits"></a>
# **listRepoCommits**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listRepoCommits(owner, repo, branch, limit)

List commits on a repository.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val branch : kotlin.String = branch_example // kotlin.String | 
val limit : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listRepoCommits(owner, repo, branch, limit)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#listRepoCommits")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#listRepoCommits")
    e.printStackTrace()
}
```

### Parameters
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
| **branch** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **kotlin.Int**|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listRepoPullRequests"></a>
# **listRepoPullRequests**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listRepoPullRequests(owner, repo)

List pull requests on a repository.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listRepoPullRequests(owner, repo)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#listRepoPullRequests")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#listRepoPullRequests")
    e.printStackTrace()
}
```

### Parameters
| **owner** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **repo** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listRepoRepositories"></a>
# **listRepoRepositories**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listRepoRepositories(visibility, limit)

List the caller&#39;s accessible repositories.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val visibility : kotlin.String = visibility_example // kotlin.String | 
val limit : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listRepoRepositories(visibility, limit)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#listRepoRepositories")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#listRepoRepositories")
    e.printStackTrace()
}
```

### Parameters
| **visibility** | **kotlin.String**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **kotlin.Int**|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listRepoTasks"></a>
# **listRepoTasks**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listRepoTasks(owner, repo, state, perPage, page)

List tasks linked to this repo (the \&quot;issues\&quot; surface).

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val state : kotlin.String = state_example // kotlin.String | 
val perPage : kotlin.Int = 56 // kotlin.Int | 
val page : kotlin.Int = 56 // kotlin.Int | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listRepoTasks(owner, repo, state, perPage, page)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#listRepoTasks")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#listRepoTasks")
    e.printStackTrace()
}
```

### Parameters
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
| **state** | **kotlin.String**|  | [optional] [enum: open, closed, all] |
| **perPage** | **kotlin.Int**|  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **kotlin.Int**|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="listRepoWorkflows"></a>
# **listRepoWorkflows**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; listRepoWorkflows(owner, repo)

List CI workflows.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.listRepoWorkflows(owner, repo)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#listRepoWorkflows")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#listRepoWorkflows")
    e.printStackTrace()
}
```

### Parameters
| **owner** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **repo** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="mergeRepoPullRequest"></a>
# **mergeRepoPullRequest**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; mergeRepoPullRequest(owner, repo, number, requestBody)

Merge a pull request.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val number : kotlin.Int = 56 // kotlin.Int | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.mergeRepoPullRequest(owner, repo, number, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#mergeRepoPullRequest")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#mergeRepoPullRequest")
    e.printStackTrace()
}
```

### Parameters
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
| **number** | **kotlin.Int**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **requestBody** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="triggerRepoWorkflow"></a>
# **triggerRepoWorkflow**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; triggerRepoWorkflow(owner, repo, id, requestBody)

Trigger a workflow_dispatch run.

### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.triggerRepoWorkflow(owner, repo, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#triggerRepoWorkflow")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#triggerRepoWorkflow")
    e.printStackTrace()
}
```

### Parameters
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **requestBody** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceCreateRepoBranch"></a>
# **workspaceCreateRepoBranch**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateRepoBranch(org, workspace, owner, repo, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateRepoBranch(org, workspace, owner, repo, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceCreateRepoBranch")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceCreateRepoBranch")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
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

<a id="workspaceCreateRepoPullRequest"></a>
# **workspaceCreateRepoPullRequest**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateRepoPullRequest(org, workspace, owner, repo, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateRepoPullRequest(org, workspace, owner, repo, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceCreateRepoPullRequest")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceCreateRepoPullRequest")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
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

<a id="workspaceCreateRepoRepository"></a>
# **workspaceCreateRepoRepository**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceCreateRepoRepository(org, workspace, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceCreateRepoRepository(org, workspace, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceCreateRepoRepository")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceCreateRepoRepository")
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

<a id="workspaceGetRepoCommit"></a>
# **workspaceGetRepoCommit**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetRepoCommit(org, workspace, owner, repo, sha)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val sha : kotlin.String = sha_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetRepoCommit(org, workspace, owner, repo, sha)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceGetRepoCommit")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceGetRepoCommit")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sha** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceGetRepoRepository"></a>
# **workspaceGetRepoRepository**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceGetRepoRepository(org, workspace, owner, repo)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceGetRepoRepository(org, workspace, owner, repo)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceGetRepoRepository")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceGetRepoRepository")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **owner** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **repo** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceLinkRepoTask"></a>
# **workspaceLinkRepoTask**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceLinkRepoTask(org, workspace, owner, repo, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceLinkRepoTask(org, workspace, owner, repo, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceLinkRepoTask")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceLinkRepoTask")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
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

<a id="workspaceListRepoBranches"></a>
# **workspaceListRepoBranches**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListRepoBranches(org, workspace, owner, repo)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListRepoBranches(org, workspace, owner, repo)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceListRepoBranches")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceListRepoBranches")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **owner** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **repo** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceListRepoCommits"></a>
# **workspaceListRepoCommits**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListRepoCommits(org, workspace, owner, repo)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListRepoCommits(org, workspace, owner, repo)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceListRepoCommits")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceListRepoCommits")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **owner** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **repo** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceListRepoPullRequests"></a>
# **workspaceListRepoPullRequests**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListRepoPullRequests(org, workspace, owner, repo)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListRepoPullRequests(org, workspace, owner, repo)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceListRepoPullRequests")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceListRepoPullRequests")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **owner** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **repo** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceListRepoRepositories"></a>
# **workspaceListRepoRepositories**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListRepoRepositories(org, workspace)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListRepoRepositories(org, workspace)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceListRepoRepositories")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceListRepoRepositories")
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

<a id="workspaceListRepoTasks"></a>
# **workspaceListRepoTasks**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListRepoTasks(org, workspace, owner, repo)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListRepoTasks(org, workspace, owner, repo)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceListRepoTasks")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceListRepoTasks")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **owner** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **repo** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceListRepoWorkflows"></a>
# **workspaceListRepoWorkflows**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceListRepoWorkflows(org, workspace, owner, repo)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceListRepoWorkflows(org, workspace, owner, repo)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceListRepoWorkflows")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceListRepoWorkflows")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **owner** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **repo** | **kotlin.String**|  | |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="workspaceMergeRepoPullRequest"></a>
# **workspaceMergeRepoPullRequest**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceMergeRepoPullRequest(org, workspace, owner, repo, number, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val number : kotlin.Int = 56 // kotlin.Int | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceMergeRepoPullRequest(org, workspace, owner, repo, number, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceMergeRepoPullRequest")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceMergeRepoPullRequest")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
| **number** | **kotlin.Int**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **requestBody** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="workspaceTriggerRepoWorkflow"></a>
# **workspaceTriggerRepoWorkflow**
> kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt; workspaceTriggerRepoWorkflow(org, workspace, owner, repo, id, requestBody)



### Example
```kotlin
// Import classes:
//import app.spatio.client.infrastructure.*
//import app.spatio.client.models.*

val apiInstance = RepoApi()
val org : kotlin.String = org_example // kotlin.String | 
val workspace : kotlin.String = workspace_example // kotlin.String | 
val owner : kotlin.String = owner_example // kotlin.String | 
val repo : kotlin.String = repo_example // kotlin.String | 
val id : kotlin.String = id_example // kotlin.String | 
val requestBody : kotlin.collections.Map<kotlin.String, kotlin.Any> = Object // kotlin.collections.Map<kotlin.String, kotlin.Any> | 
try {
    val result : kotlin.collections.Map<kotlin.String, kotlin.Any> = apiInstance.workspaceTriggerRepoWorkflow(org, workspace, owner, repo, id, requestBody)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling RepoApi#workspaceTriggerRepoWorkflow")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling RepoApi#workspaceTriggerRepoWorkflow")
    e.printStackTrace()
}
```

### Parameters
| **org** | **kotlin.String**|  | |
| **workspace** | **kotlin.String**|  | |
| **owner** | **kotlin.String**|  | |
| **repo** | **kotlin.String**|  | |
| **id** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **requestBody** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)|  | [optional] |

### Return type

[**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

