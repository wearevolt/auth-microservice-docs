## Authentication [/api/v1/authentications]
Sign in using email, password and device type. Responds with refresh token.
### Sign In [POST]

+ Request Successful sign in for non web application (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `authentications` (string, required)
            + attributes (required)
                + email: `foo@bar.com`        (string, required) - User's email
                + password:  `test-password`  (string, required) - User's password
                + `device-type`: `curl`       (enum, required) - Device type
                    + curl    (string) - For scripting and debuging purposes
                    + web     (string) - For web browsers. Token will be sent in HTTP Only Cookies and will be unavailable for common js api.
                    + android (string) - For android devices
                    + ios     (string) - For iOS devices
            
                
+ Response 200 (application/json; charset=utf-8)
    + Headers

            RefreshToken: <Encoded Refresh Token>

    + Attributes (object)
        + data
            + type: `authentications` (string)
            + id                      (string)
            + attributes
                + `email` (string)
                + `device_type` (string)
                
+ Request Successful sign in for web application (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `authentications` (string, required)
            + attributes (required)
                + email: `foo@bar.com`        (string, required) - User's email
                + password:  `test-password`  (string, required) - User's password
                + `device-type`: `web`        (string, required) - Device type
                
+ Response 200 (application/json; charset=utf-8)
    + Headers

            Set-Cookie:  RefreshToken=<Encoded Refresh Token>; HttpOnly

    + Attributes (object)
        + data
            + type: `authentications` (string)
            + id                      (string)
            + attributes
                + `email` (string)
                + `device_type` (string)
                
+ Request failed (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `authentications` (string, required)
            + attributes (required)
                + email:     `wrong@email.com`      (string, required) - User's email
                + password:  `invalidpassword`  (string, required) - User's password
                + `device-type`: `curl`

+ Response 401 (application/json; charset=utf-8)
    + Attributes (object)
        + errors (array)
            + (object)
                + status: 401 (number)
                + title: `Wrong email or password given` (string)

## End session [/api/v1/authentications ]
Remove token JTI from Redis.
### Withdraw Refresh token [DELETE]

+ Request (application/vnd.api+json)
    + Headers
    
            Authorization: Bearer <Encoded Refresh Token>
        
+ Response 204 (application/json; charset=utf-8)