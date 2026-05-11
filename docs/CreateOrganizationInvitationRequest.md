
# CreateOrganizationInvitationRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **email** | **kotlin.String** |  |  |
| **role** | [**inline**](#Role) |  |  |
| **workspaceId** | **kotlin.String** | Optional — the invitee will also be added to this workspace on accept. Defaults to the org&#39;s default workspace.  |  [optional] |


<a id="Role"></a>
## Enum: role
| Name | Value |
| ---- | ----- |
| role | owner, admin, billing_admin, member |



