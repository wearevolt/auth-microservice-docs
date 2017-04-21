## Email confirmation [/api/v1/emails/confirm]
Confirm email address by token.
### Confirm [POST]

+ Request for web applications (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + confirmation-token: `token` (string) - Confirmation token string
                + device-type: `web`          (string) - Device type  

+ Response 200 (application/json; charset=utf-8)
    + Headers

            Set-Cookie:  RefreshToken=<Encoded Refresh Token>; HttpOnly - return refresh token for web applications in cookies

    + Attributes (object)
            + data (object)
                + id (string)
                + type: `emails`
                + attributes (object)
                    + value      (string)  - email value
                    + confirmed  (boolean) - confirmed status

+ Request ror non web applications (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + confirmation-token: `token` (string) - Confirmation token string
                + device-type: `curl`         (string) - Device type  

+ Response 200 (application/json; charset=utf-8)
    + Headers

            RefreshToken: <Encoded Refresh Token> - return refresh token for non web application in headers

    + Attributes (object)
            + data (object)
                + id (string)
                + type: `emails`
                + attributes (object)
                    + value      (string)  - email value
                    + confirmed  (boolean) - confirmed status
                    
+ Request failed (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + confirmation-token: `invalid token` (string) - Confirmation token string
                + device-type: `web`                  (string) - Device type
                  
+ Response 401 (application/json; charset=utf-8)
    + Attributes (object)
        + errors (array)
            + (object)
                + status: 401 (number)
                + title: `Invalid Token` (string)

## Request confirmation token [/api/v1/emails/request-confirmation-token]
Request confirmation token to specified email.
### Request confirmation token [POST]

+ Request (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + email: `qwe@rty.com` (string) - Email value

+ Response 204 (application/json; charset=utf-8)

+ Request (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + email: `wrong@email.com` (string) - Email value

+ Response 404 (application/json; charset=utf-8)
    + Attributes (object)
        + errors (array)
            + (object)
                + status: 404 (number)
                + title: `invalid Email` (string)