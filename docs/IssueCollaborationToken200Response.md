
# IssueCollaborationToken200Response

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **token** | **kotlin.String** | HS256 JWT, signed with the shared platform/worker secret. |  |
| **wsUrl** | **kotlin.String** | Base WebSocket URL of the Yjs worker. |  |
| **expiresAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **expiresIn** | **kotlin.Int** | Seconds until the token expires. |  |
| **room** | **kotlin.String** |  |  [optional] |



