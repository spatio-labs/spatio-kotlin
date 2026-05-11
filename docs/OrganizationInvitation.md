
# OrganizationInvitation

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** |  |  |
| **email** | **kotlin.String** |  |  |
| **role** | **kotlin.String** |  |  |
| **createdAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **organizationId** | **kotlin.String** |  |  [optional] |
| **token** | **kotlin.String** | Opaque invitation token (omitted on list responses). |  [optional] |
| **expiresAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **acceptedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **revokedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **invitedBy** | [**OrganizationMemberInvitedBy**](OrganizationMemberInvitedBy.md) |  |  [optional] |
| **status** | [**inline**](#Status) |  |  [optional] |


<a id="Status"></a>
## Enum: status
| Name | Value |
| ---- | ----- |
| status | pending, accepted, revoked, expired |



