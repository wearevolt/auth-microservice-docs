## Admin Emails [/api/v1/admin/emails]

###Relations

###has_one
+ user
+ facebook

### Get All Emails [GET /api/v1/admin/emails]

+ Request (application/vnd.api+json)

    + Headers

            Authorization:  Bearer <Api Token>

+ Response 200 (application/vnd.api+json)
            
            {
                "data"=>
                    [
                        {
                            "id"=>"42b6cfc2-5ee9-45b7-a031-aae5ffee3718",
                            "type"=>"emails",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/emails/42b6cfc2-5ee9-45b7-a031-aae5ffee3718"},
                            "attributes"=>{"value"=>"maud@corwinmann.com", "confirmed"=>true},
                            "relationships"=>
                                {
                                    "user"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/emails/42b6cfc2-5ee9-45b7-a031-aae5ffee3718/relationships/user",
                                                    "related"=>"http://www.example.com/api/v1/admin/emails/42b6cfc2-5ee9-45b7-a031-aae5ffee3718/user"
                                                }
                                            }
                                        }
                                    "facebook"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/emails/42b6cfc2-5ee9-45b7-a031-aae5ffee3718/relationships/facebook",
                                                    "related"=>"http://www.example.com/api/v1/admin/emails/42b6cfc2-5ee9-45b7-a031-aae5ffee3718/facebook"
                                                }
                                            }
                                        }    
                                },
                        {
                            "id"=>"7f5e1704-3c7b-4357-916d-d4b76c42efa1",
                            "type"=>"emails",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/emails/7f5e1704-3c7b-4357-916d-d4b76c42efa1"},
                            "attributes"=>{"value"=>"jonas_bauch@moen.info", "confirmed"=>true},
                            "relationships"=>
                                {
                                    "user"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/emails/7f5e1704-3c7b-4357-916d-d4b76c42efa1/relationships/user",
                                                    "related"=>"http://www.example.com/api/v1/admin/emails/7f5e1704-3c7b-4357-916d-d4b76c42efa1/user"
                                                }
                                            }
                                        }
                                    "facebook"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/emails/7f5e1704-3c7b-4357-916d-d4b76c42efa1/relationships/facebook",
                                                    "related"=>"http://www.example.com/api/v1/admin/emails/7f5e1704-3c7b-4357-916d-d4b76c42efa1/facebook"
                                                }
                                            }
                                        }    
                                },
                        {
                            "id"=>"ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4",
                            "type"=>"emails",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/emails/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4"},
                            "attributes"=>{"value"=>"dora@hartmann.name", "confirmed"=>true},
                            "relationships"=>
                                {
                                    "user"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/emails/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4/relationships/user",
                                                    "related"=>"http://www.example.com/api/v1/admin/emails/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4/user"
                                                }
                                            }
                                        }
                                    "facebook"=>
                                     {
                                         "links"=>
                                             {
                                                 "self"=>"http://www.example.com/api/v1/admin/emails/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4/relationships/facebook",
                                                 "related"=>"http://www.example.com/api/v1/admin/emails/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4/facebook"
                                             }
                                         }
                                     }   
                                }
                    ]
            }

### Get Email [GET /api/v1/admin/emails/{email_id}]

+ Parameters
    + `email_id`: 1 (string) - Email Id

+ Request (application/vnd.api+json)

    + Headers

            Authorization:  Bearer <Api Token>

+ Response 200 (application/vnd.api+json)

          {
              "data"=>
                  {
                      "id"=>"42afb9e3-c5bb-4c0a-ac3c-8b4fd388965d",
                      "type"=>"emails",
                      "links"=>{"self"=>"http://www.example.com/api/v1/admin/emails/42afb9e3-c5bb-4c0a-ac3c-8b4fd388965d"},
                      "attributes"=>{"value"=>"dagmar_metz@willms.com", "confirmed"=>true},
                      "relationships"=>
                          {
                              "user"=>
                                  {
                                      "links"=>
                                          {
                                              "self"=>"http://www.example.com/api/v1/admin/emails/42afb9e3-c5bb-4c0a-ac3c-8b4fd388965d/relationships/user",
                                              "related"=>"http://www.example.com/api/v1/admin/emails/42afb9e3-c5bb-4c0a-ac3c-8b4fd388965d/user"
                                          }
                                  }
                              "facebook"=>
                                  {
                                      "links"=>
                                          {
                                              "self"=>"http://www.example.com/api/v1/admin/emails/42afb9e3-c5bb-4c0a-ac3c-8b4fd388965d/relationships/facebook",
                                              "related"=>"http://www.example.com/api/v1/admin/emails/42afb9e3-c5bb-4c0a-ac3c-8b4fd388965d/facebook"
                                          }
                                  }    
                          }
                  }
          }

### Delete Email [DELETE /api/v1/admin/emails/{email_id}]

+ Parameters
    + email_id: 1 (string) - Email Id

+ Request (application/vnd.api+json)

    + Headers

            Authorization:  Bearer <Api Token>

+ Response 204 (application/vnd.api+json)