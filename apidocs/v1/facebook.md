## Add Facebook email [/api/v1/facebooks]
Add facebook email to requested user emails.
### Register Facebook email [POST]

+ Request for web applications (application/vnd.api+json)
    + Headers

            Authorization:  Bearer <Api Token>

    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + `access-token`: `access-token` (string) - Facebook access token  

+ Response 200 (application/json; charset=utf-8)

    + Attributes (object)
        + data (object)
            + id (string)
            + type: `facebooks`
            + attributes (object)
                + uid      (string)  - facebook user id

+ Request failed (application/vnd.api+json)
    + Headers

            Authorization:  Bearer <Api Token>

    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + `access-token`: `wrong access token` (string) - Wrong facebook access token  
  
+ Response 403 (application/json; charset=utf-8)
    + Attributes (object)
        + errors (array)
            + (object)
                + status: 403 (number)
                + title: `Error title` (string)
                + detail: `Error details` (string)
                + code: `Error code` (string)
                + source: `Error source` (string)
                
## Remove associated facebook email [/api/v1/facebooks/{uuid}]
Remove requested user's facebook email by uuid.
+ Parameters
    + uuid (required, integer, `d7a836aa-32bd-4318-a60d-a01f46f72176`)
    
### Delete facebook email [DELETE]

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