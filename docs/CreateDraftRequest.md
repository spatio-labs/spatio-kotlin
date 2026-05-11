
# CreateDraftRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **accountId** | **kotlin.String** |  |  [optional] |
| **to** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **cc** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **bcc** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **subject** | **kotlin.String** |  |  [optional] |
| **body** | **kotlin.String** |  |  [optional] |
| **html** | **kotlin.Boolean** |  |  [optional] |
| **attachments** | [**kotlin.collections.List&lt;AttachmentInput&gt;**](AttachmentInput.md) |  |  [optional] |
| **threadId** | **kotlin.String** | Provider thread id — set when this draft is a reply, so the sent message lands inside the parent thread.  |  [optional] |
| **inReplyTo** | **kotlin.String** |  |  [optional] |
| **references** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |



