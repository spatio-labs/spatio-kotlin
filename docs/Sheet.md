
# Sheet

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** |  |  |
| **name** | **kotlin.String** |  |  |
| **rowCount** | **kotlin.Int** |  |  |
| **columnCount** | **kotlin.Int** |  |  |
| **sheetCount** | **kotlin.Int** | Tab count when the file contains multiple sheets. |  |
| **isPublic** | **kotlin.Boolean** |  |  |
| **isReadOnly** | **kotlin.Boolean** |  |  |
| **createdAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **updatedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **provider** | **kotlin.String** | Registered provider id (e.g. &#x60;native-sheets&#x60;). |  [optional] |
| **accountId** | **kotlin.String** | Connected-account row this sheet belongs to. |  [optional] |
| **ownerUserId** | **kotlin.String** | User id of the sheet owner; non-native providers leave empty. |  [optional] |
| **description** | **kotlin.String** |  |  [optional] |
| **&#x60;data&#x60;** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md) | Free-form provider blob. Treat as opaque. |  [optional] |
| **fileSize** | **kotlin.Int** |  |  [optional] |
| **lastAccessedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |



