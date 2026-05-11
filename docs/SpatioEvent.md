
# SpatioEvent

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** |  |  |
| **title** | **kotlin.String** |  |  |
| **startTime** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **endTime** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **allDay** | **kotlin.Boolean** |  |  |
| **status** | **kotlin.String** | Provider-mapped event status. Free-form string — common values are &#x60;confirmed&#x60;, &#x60;tentative&#x60;, &#x60;cancelled&#x60;, &#x60;needs_action&#x60;, and the empty string when the provider doesn&#39;t populate it. Not enumerated strictly because providers add custom values and the platform passes them through verbatim.  |  |
| **visibility** | **kotlin.String** | Free-form visibility string. Common values: &#x60;public&#x60;, &#x60;private&#x60;, &#x60;confidential&#x60;, plus empty when unset.  |  |
| **busy** | **kotlin.Boolean** | Whether this event marks the time as busy or free. |  |
| **accountId** | **kotlin.String** |  |  |
| **providerId** | **kotlin.String** | Legacy alias of &#x60;provider&#x60;. |  |
| **createdAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **updatedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  |
| **description** | **kotlin.String** |  |  [optional] |
| **location** | **kotlin.String** |  |  [optional] |
| **locationDetails** | **kotlin.collections.Map&lt;kotlin.String, kotlin.String&gt;** | Free-form key/value (lat, lng, room, etc.). |  [optional] |
| **organizer** | **kotlin.String** | Organizer email. |  [optional] |
| **attendees** | [**kotlin.collections.List&lt;Attendee&gt;**](Attendee.md) |  |  [optional] |
| **recurrenceRule** | **kotlin.String** | RFC 5545 RRULE. |  [optional] |
| **recurrenceId** | **kotlin.String** | Set on instances of a recurring series. |  [optional] |
| **originalStart** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) | Original start of a moved recurring instance. |  [optional] |
| **reminders** | [**kotlin.collections.List&lt;Reminder&gt;**](Reminder.md) |  |  [optional] |
| **travelTimeMinutes** | **kotlin.Int** | Apple Calendar&#39;s local-only travel buffer. Stored on the cached row but not synced to providers that don&#39;t model it.  |  [optional] |
| **categories** | **kotlin.collections.List&lt;kotlin.String&gt;** |  |  [optional] |
| **color** | **kotlin.String** |  |  [optional] |
| **userId** | **kotlin.String** |  |  [optional] |
| **provider** | **kotlin.String** | Standardized provider id (e.g. &#x60;google-calendar&#x60;, &#x60;native-calendar&#x60;). Mirrors &#x60;provider_id&#x60; — both are populated on writes; clients should prefer &#x60;provider&#x60;.  |  [optional] |
| **providerData** | [**kotlin.collections.Map&lt;kotlin.String, kotlin.Any&gt;**](kotlin.Any.md) | Provider-specific extras. |  [optional] |
| **deletedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **syncedAt** | [**java.time.OffsetDateTime**](java.time.OffsetDateTime.md) |  |  [optional] |
| **conferenceData** | [**ConferenceData**](ConferenceData.md) |  |  [optional] |
| **attachments** | [**kotlin.collections.List&lt;Attachment&gt;**](Attachment.md) |  |  [optional] |
| **url** | [**java.net.URI**](java.net.URI.md) |  |  [optional] |
| **etag** | **kotlin.String** |  |  [optional] |
| **sequence** | **kotlin.Int** |  |  [optional] |
| **customData** | **kotlin.collections.Map&lt;kotlin.String, kotlin.String&gt;** |  |  [optional] |



