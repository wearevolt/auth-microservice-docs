## API token [/api/v1/api-tokens]
Returns updated refresh token and new api token(for web only applications).
### Get API token [POST]

+ Request Successful for non web application (application/vnd.api+json)
    + Headers
    
            Authorization: Bearer <Encoded Refresh Token>

    + Attributes
        + data (required)
            + type: `api-tokens` (string, required)
        
+ Response 200 (application/json; charset=utf-8)
    + Headers

            RefreshToken: <Encoded Refresh Token> - should return updated refresh token for non web application
            
    + Attributes (object)
            + data (object)
                + id (string)
                + type: `api-tokens`
                + attributes (object)
                    + value      (string) - API token string
                    + issued-at  (string) - issued time
                    + expires-at (string) - expiration time

+ Request Successful for web application (application/vnd.api+json)
    + Headers
    
            Authorization: Bearer <Encoded Refresh Token>

    + Attributes
        + data (required)
            + type: `api-tokens` (string, required)
        
+ Response 200 (application/json; charset=utf-8)
    + Headers

            Set-Cookie:  RefreshToken=<Encoded Refresh Token>; HttpOnly - return updated refresh token
            Set-Cookie:  ApiToken=<Encoded Api Token>; HttpOnly
            
    + Attributes (object)
            + data (object)
                + id (string)
                + type: `api-tokens`
                + attributes (object)
                    + value      (string) - API token string
                    + issued-at  (string) - issued time
                    + expires-at (string) - expiration time
