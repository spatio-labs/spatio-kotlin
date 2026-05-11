
# CreateEventRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String** |  |  |
| **event** | [**SpatioEvent**](SpatioEvent.md) |  |  |
| **calendarId** | **kotlin.String** | Specific calendar within the account; omit for the default. |  [optional] |
| **sendUpdates** | [**inline**](#SendUpdates) | Notification policy passed through to the provider. |  [optional] |
| **conferenceType** | **kotlin.String** | When set, the platform will auto-attach a conference link of the matching type (&#x60;spatio&#x60;, &#x60;meet&#x60;, &#x60;zoom&#x60;, &#x60;teams&#x60;).  |  [optional] |


<a id="SendUpdates"></a>
## Enum: send_updates
| Name | Value |
| ---- | ----- |
| sendUpdates | all, externalOnly, none |



