
# OrganizationMember

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** | &#x60;OrganizationMember&#x60; row id. |  |
| **userId** | **kotlin.String** |  |  |
| **role** | [**inline**](#Role) |  |  |
| **joinedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **invitedBy** | [**OrganizationMemberInvitedBy**](OrganizationMemberInvitedBy.md) |  |  [optional] |
| **user** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md) | Embedded user-profile fields (id, email, name, profilePhoto, ...). |  [optional] |


<a id="Role"></a>
## Enum: role
| Name | Value |
| ---- | ----- |
| role | owner, admin, billing_admin, member |



