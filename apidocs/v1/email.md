## Email creation [/api/v1/emails]
Add new email address for requested user and send confirmation message on it.
### Add new email address [POST]

+ Request for web applications (application/vnd.api+json)
    + Headers

            Authorization:  Bearer <Api Token>

    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + `value`: `foo@bar.com` (string) - Email address string  

+ Response 200 (application/json; charset=utf-8)

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
                + `value`: `invalid email` (string) - Wrong Email address string  
                  
+ Response 422 (application/json; charset=utf-8)
    + Attributes (object)
        + errors (array)
            + (object)
                + status: 422 (number)
                + title: `Error title` (string)
                + detail: `Error details` (string)
                + code: `Error code` (string)
                + source: `Error source` (string)

## Remove associated email for requested user [/api/v1/emails/{uuid}]
Remove requested user's email by uuid.
+ Parameters
    + uuid (required, integer, `d7a836aa-32bd-4318-a60d-a01f46f72176`)
    
### Delete email address [DELETE]

+ Request for web applications (application/vnd.api+json)
    + Headers

            Authorization:  Bearer <Api Token>

+ Response 204 (application/json; charset=utf-8)

+ Request failed (application/vnd.api+json)
    
            Authorization:  Bearer <Api Token>

+ Response 403 (application/json; charset=utf-8)
    + Attributes (object)
        + errors (array)
            + (object)
                + status: 403 (number)
                + title: `Error title` (string)
                + detail: `Error details` (string)
                + code: `Error code` (string)
                + source: `Error source` (string)

## Email confirmation [/api/v1/emails/confirm]
Confirm email address by token.
### Confirm [POST]

+ Request for web applications (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + `confirmation-token`: `token` (string) - Confirmation token string
                + `device-type`: `web`          (string) - Device type  

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

+ Request for non web applications (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + `confirmation-token`: `token` (string) - Confirmation token string
                + `device-type`: `curl`         (string) - Device type  

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
                + `confirmation-token`: `invalid token` (string) - Confirmation token string
                + `device-type`: `web`                  (string) - Device type
                  
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