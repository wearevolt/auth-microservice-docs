## Registration [/api/v1/users]
Registers a new user with given emails, password and fullname.
### Register a user [POST]

+ Request (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `users` (required)
            + attributes (required):
                + `full-name`: `Test User`        (string, required) - User's fullname
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
                + `full-name`          (string)

+ Request (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `users` (required)
            + attributes (required):
                + `full-name`: `Test`            (string) - User's fullname
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
                + `full-name`          (string)

## Reset Password [/api/v1/users/send-password-reset-token]
Request reset password token to specified email.
### Send password reset token [POST]

+ Request (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `users` (string, required)
            + attributes (object)
                + email: `qwe@rty.com` (string) - Email value

+ Response 204 (application/json; charset=utf-8)

## Set Password [/api/v1/users/send-password-by-token]
Set new password by reset password token
### Set password by reset token [POST]

+ Request (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `users` (string, required)
            + attributes (object)
                + `reset-password-token`: `token` (string) - Reset password token string
                + password: `abcd1234`          (string) - New valid password
                
+ Response 204 (application/json; charset=utf-8)

+ Request failed (application/vnd.api+json)
    + Attributes
        + data (required)
            + type: `emails` (string, required)
            + attributes (object)
                + `reset-password-token`: `token` (string) - Reset password token string
                + password: `abcd`              (string) - Wrong new valid password

+ Response 422 (application/json; charset=utf-8)
    + Attributes (object)
        + errors (array)
            + (object)
                + status: 422 (number)
                + title: `wrong password` (string)

