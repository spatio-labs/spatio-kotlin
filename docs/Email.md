
# Email

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** |  |  |
| **subject** | **kotlin.String** |  |  |
| **from** | **kotlin.String** |  |  |
| **to** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  |
| **body** | **kotlin.String** |  |  |
| **html** | **kotlin.Boolean** | &#x60;true&#x60; when &#x60;body&#x60; contains HTML, &#x60;false&#x60; for plain text.  |  |
| **date** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **isRead** | **kotlin.Boolean** |  |  |
| **isStarred** | **kotlin.Boolean** |  |  |
| **threadId** | **kotlin.String** |  |  [optional] |
| **provider** | **kotlin.String** |  |  [optional] |
| **accountId** | **kotlin.String** |  |  [optional] |
| **cc** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **bcc** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **labels** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **attachments** | [**kotlin.collections.List&lt;AttachmentMeta&gt;**](AttachmentMeta.md) |  |  [optional] |
| **snippet** | **kotlin.String** |  |  [optional] |
| **messageId** | **kotlin.String** | RFC 5322 Message-ID header. |  [optional] |
| **inReplyTo** | **kotlin.String** | RFC 5322 In-Reply-To header — the parent message id this message is a reply to.  |  [optional] |
| **references** | **kotlin.collections.List&lt;kotlin.String&gt;** | RFC 5322 References header (ancestor chain). |  [optional] |



