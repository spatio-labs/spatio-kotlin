
# BlockContent

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **richText** | [**kotlin.collections.List&lt;RichTextObject&gt;**](RichTextObject.md) |  |  [optional] |
| **language** | **kotlin.String** | Programming language for &#x60;code&#x60; blocks. |  [optional] |
| **checked** | **kotlin.Boolean** | Toggle state for &#x60;to_do&#x60; blocks. |  [optional] |
| **icon** | **kotlin.String** | Emoji or short string for &#x60;callout&#x60; blocks. |  [optional] |
| **color** | **kotlin.String** | Theme color for &#x60;callout&#x60; blocks. |  [optional] |
| **url** | [**java.net.URI**](java.net.URI.md) | Source URL for &#x60;image&#x60;, &#x60;video&#x60;, &#x60;file&#x60; blocks. |  [optional] |
| **caption** | **kotlin.String** | Visible caption for media blocks. |  [optional] |
| **altText** | **kotlin.String** | Screen-reader description for media blocks. Distinct from &#x60;caption&#x60; (visible to readers) — required for accessible notes when the image conveys meaning.  |  [optional] |
| **embedUrl** | [**java.net.URI**](java.net.URI.md) | Source URL for &#x60;embed&#x60; blocks. |  [optional] |
| **cells** | **kotlin.collections.List&lt;kotlin.collections.List&lt;RichTextObject&gt;&gt;** | 2D rich-text grid for &#x60;table&#x60; and &#x60;table_row&#x60; blocks. |  [optional] |
| **expression** | **kotlin.String** | TeX/MathJax expression for &#x60;equation&#x60; blocks. |  [optional] |



