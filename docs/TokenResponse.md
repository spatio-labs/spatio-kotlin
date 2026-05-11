
# TokenResponse

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **accessToken** | **kotlin.String** | Opaque bearer token. Format &#x60;tok_&lt;32 random base64url&gt;&#x60;. |  |
| **tokenType** | **kotlin.String** |  |  |
| **expiresIn** | **kotlin.Int** | Seconds until access_token expires. |  |
| **refreshToken** | **kotlin.String** |  |  [optional] |
| **scope** | **kotlin.String** |  |  [optional] |
| **idToken** | **kotlin.String** | Only present when &#x60;openid&#x60; scope was granted. RS256-signed JWT — verify against the JWKS. |  [optional] |



