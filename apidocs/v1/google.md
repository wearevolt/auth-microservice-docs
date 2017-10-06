## Add Facebook email [/api/v1/googles]
Add google email to requested user emails.
### Register Google email [POST]

+ Request for web applications (application/vnd.api+json)
    + Headers

            Authorization:  Bearer <Api Token>

    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + `id-token`: `id-token` (string) - Google id token  

+ Response 200 (application/json; charset=utf-8)

    + Attributes (object)
        + data (object)
            + id (string)
            + type: `googles`
            + attributes (object)
                + uid      (string)  - google user id

+ Request failed (application/vnd.api+json)
    + Headers

            Authorization:  Bearer <Api Token>

    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + `id-token`: `wrong id token` (string) - Wrong google id token  
  
+ Response 403 (application/json; charset=utf-8)
    + Attributes (object)
        + errors (array)
            + (object)
                + status: 403 (number)
                + title: `Error title` (string)
                + detail: `Error details` (string)
                + code: `Error code` (string)
                + source: `Error source` (string)
                
## Remove associated google email [/api/v1/googles/{uuid}]
Remove requested user's google email by uuid.
+ Parameters
    + uuid (required, integer, `d7a836aa-32bd-4318-a60d-a01f46f72176`)
    
### Delete google email [DELETE]

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