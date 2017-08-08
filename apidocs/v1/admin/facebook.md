## Admin Facebooks [/api/v1/admin/facebooks]

###Relations

###has_one
+ user
+ email

### Get All Facebooks [GET /api/v1/admin/facebook]

+ Request (application/vnd.api+json)

    + Headers

            Authorization:  Bearer <Api Token>

+ Response 200 (application/vnd.api+json)
            
            {
                "data"=>
                    [
                        {
                            "id"=>"42b6cfc2-5ee9-45b7-a031-aae5ffee3718",
                            "type"=>"facebooks",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/facebooks/42b6cfc2-5ee9-45b7-a031-aae5ffee3718"},
                            "attributes"=>{"uid"=>"42b6cfc2-5ee9-45b7-a031-aae5ffee3718"},
                            "relationships"=>
                                {
                                    "user"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/facebooks/42b6cfc2-5ee9-45b7-a031-aae5ffee3718/relationships/user",
                                                    "related"=>"http://www.example.com/api/v1/admin/facebooks/42b6cfc2-5ee9-45b7-a031-aae5ffee3718/user"
                                                }
                                            }
                                        }
                                    "email"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/facebooks/42b6cfc2-5ee9-45b7-a031-aae5ffee3718/relationships/email",
                                                    "related"=>"http://www.example.com/api/v1/admin/facebooks/42b6cfc2-5ee9-45b7-a031-aae5ffee3718/email"
                                                }
                                            }
                                        }    
                                },
                        {
                            "id"=>"7f5e1704-3c7b-4357-916d-d4b76c42efa1",
                            "type"=>"facebooks",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/facebooks/7f5e1704-3c7b-4357-916d-d4b76c42efa1"},
                            "attributes"=>{"uid"=>"7f5e1704-3c7b-4357-916d-d4b76c42efa1"},
                            "relationships"=>
                                {
                                    "user"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/facebooks/7f5e1704-3c7b-4357-916d-d4b76c42efa1/relationships/user",
                                                    "related"=>"http://www.example.com/api/v1/admin/facebooks/7f5e1704-3c7b-4357-916d-d4b76c42efa1/user"
                                                }
                                            }
                                        }
                                    "email"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/facebooks/7f5e1704-3c7b-4357-916d-d4b76c42efa1/relationships/email",
                                                    "related"=>"http://www.example.com/api/v1/admin/facebooks/7f5e1704-3c7b-4357-916d-d4b76c42efa1/email"
                                                }
                                            }
                                        }    
                                },
                        {
                            "id"=>"ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4",
                            "type"=>"facebooks",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/facebooks/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4"},
                            "attributes"=>{"uid"=>"ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4"},
                            "relationships"=>
                                {
                                    "user"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/facebooks/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4/relationships/user",
                                                    "related"=>"http://www.example.com/api/v1/admin/facebooks/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4/user"
                                                }
                                            }
                                        }
                                    "email"=>
                                     {
                                         "links"=>
                                             {
                                                 "self"=>"http://www.example.com/api/v1/admin/emails/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4/relationships/email",
                                                 "related"=>"http://www.example.com/api/v1/admin/emails/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4/email"
                                             }
                                         }
                                     }   
                                }
                    ]
            }

### Get Facebook [GET /api/v1/admin/facebooks/{facebook_id}]

+ Parameters
    + `facebook_id`: 1 (string) - Facebook Id

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

### Delete Facebook [DELETE /api/v1/admin/facebooks/{facebook_id}]

+ Parameters
    + facebook_id: 1 (string) - Facebook Id

+ Request (application/vnd.api+json)

    + Headers

            Authorization:  Bearer <Api Token>

+ Response 204 (application/vnd.api+json)