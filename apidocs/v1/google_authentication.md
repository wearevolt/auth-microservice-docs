## Register and/or login using Google account [/api/v1/google-authentications]
Sign in using google id token.
### Sign in through Google [POST]

+ Request Successful sign in for non web application (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `google-authentications` (string, required)
            + attributes (required)
                + id-token: `id-token` (string, required) - Google id token
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
            + type: `google-authentications` (string)
            + id                      (string)
    
+ Request Successful sign in for web application (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `google-authentications` (string, required)
            + attributes (required)
              + id-token: `id-token` (string, required) - Google id token
              + `device-type`: `web`

+ Response 200 (application/json; charset=utf-8)
    + Headers

            Set-Cookie:  RefreshToken=<Encoded Refresh Token>; HttpOnly

    + Attributes (object)
        + data
            + type: `google-authentications` (string)
            + id                      (string)
                
+ Request failed (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `google-authentications` (string, required)
            + attributes (required)
              + id-token: `wrong-id-token` (string, required) - Google id token

+ Response 403 (application/json; charset=utf-8)
    + Attributes (object)
        + errors (array)
            + (object)
                + status: 403 (number)
                + title: `Wrong id token` (string)