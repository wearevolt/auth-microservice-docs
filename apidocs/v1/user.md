## Registration [/api/v1/users]
Registers a new user with given emails, password and fullname.
### Register a user [POST]

+ Request (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `users` (required)
            + attributes (required):
                + fullname: `Test User`        (string, required) - User's fullname
                + emails:    [`foo@bar.com`]   (string, required) - User's emails)
                + password: `password`         (string, required) - User's password
                
+ Response 201 (application/vnd.api+json; charset=utf-8)
    + Attributes (object)
        + data (object)
            + id                    (string)
            + type: `users` (string)
            + links (object)
                + self: `/api/v1/users/{id}` (string)
            + attributes (object)
                + fullname          (string)

+ Request (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `users` (required)
            + attributes (required):
                + full-name: `Test`            (string) - User's fullname
                + email:    [`foo@bar.com`]   (string) - User's email
                + password: `111`             (string) - User's password
                
+ Response 422 (application/vnd.api+json; charset=utf-8)
    + Attributes (object)
        + data (object)
            + id                    (string)
            + type: `users` (string)
            + links (object)
                + self: `/api/v1/users` (string)
            + attributes (object)
                + full-name          (string)
                