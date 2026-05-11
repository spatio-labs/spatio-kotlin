
# AccountStatus

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **provider** | **kotlin.String** | Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;, &#x60;google-keep&#x60;). |  |
| **accountId** | **kotlin.String** | Connected-account row id. |  |
| **status** | [**inline**](#Status) | - &#x60;ok&#x60; — provider call returned without error. - &#x60;error&#x60; — provider call failed; details in &#x60;error&#x60;. - &#x60;skipped&#x60; — connection was filtered out before the provider   call ran. Reserved; not currently emitted by the runtime.  |  |
| **accountName** | **kotlin.String** | Human-readable label for the account, when available. |  [optional] |
| **error** | [**AccountError**](AccountError.md) |  |  [optional] |
| **nextPageToken** | **kotlin.String** | Provider-specific cursor for the next page, if any. |  [optional] |


<a id="Status"></a>
## Enum: status
| Name | Value |
| ---- | ----- |
| status | ok, error, skipped |



