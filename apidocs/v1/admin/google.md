## Admin Googles [/api/v1/admin/googles]

###Relations

###has_one
+ user
+ email

### Get All Googles [GET /api/v1/admin/googles]

+ Request (application/vnd.api+json)

    + Headers

            Authorization:  Bearer <Api Token>

+ Response 200 (application/vnd.api+json)
            
            {
                "data"=>
                    [
                        {
                            "id"=>"42b6cfc2-5ee9-45b7-a031-aae5ffee3718",
                            "type"=>"googles",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/googles/42b6cfc2-5ee9-45b7-a031-aae5ffee3718"},
                            "attributes"=>{"uid"=>"42b6cfc2-5ee9-45b7-a031-aae5ffee3718"},
                            "relationships"=>
                                {
                                    "user"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/gooles/42b6cfc2-5ee9-45b7-a031-aae5ffee3718/relationships/user",
                                                    "related"=>"http://www.example.com/api/v1/admin/googles/42b6cfc2-5ee9-45b7-a031-aae5ffee3718/user"
                                                }
                                            }
                                        }
                                    "email"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/googles/42b6cfc2-5ee9-45b7-a031-aae5ffee3718/relationships/email",
                                                    "related"=>"http://www.example.com/api/v1/admin/googles/42b6cfc2-5ee9-45b7-a031-aae5ffee3718/email"
                                                }
                                            }
                                        }    
                                },
                        {
                            "id"=>"7f5e1704-3c7b-4357-916d-d4b76c42efa1",
                            "type"=>"googles",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/googles/7f5e1704-3c7b-4357-916d-d4b76c42efa1"},
                            "attributes"=>{"uid"=>"7f5e1704-3c7b-4357-916d-d4b76c42efa1"},
                            "relationships"=>
                                {
                                    "user"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/googles/7f5e1704-3c7b-4357-916d-d4b76c42efa1/relationships/user",
                                                    "related"=>"http://www.example.com/api/v1/admin/googles/7f5e1704-3c7b-4357-916d-d4b76c42efa1/user"
                                                }
                                            }
                                        }
                                    "email"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/googles/7f5e1704-3c7b-4357-916d-d4b76c42efa1/relationships/email",
                                                    "related"=>"http://www.example.com/api/v1/admin/googles/7f5e1704-3c7b-4357-916d-d4b76c42efa1/email"
                                                }
                                            }
                                        }    
                                },
                        {
                            "id"=>"ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4",
                            "type"=>"googles",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/googles/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4"},
                            "attributes"=>{"uid"=>"ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4"},
                            "relationships"=>
                                {
                                    "user"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/googles/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4/relationships/user",
                                                    "related"=>"http://www.example.com/api/v1/admin/googles/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4/user"
                                                }
                                            }
                                        }
                                    "email"=>
                                     {
                                         "links"=>
                                             {
                                                 "self"=>"http://www.example.com/api/v1/admin/googles/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4/relationships/email",
                                                 "related"=>"http://www.example.com/api/v1/admin/googles/ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4/email"
                                             }
                                         }
                                     }   
                                }
                    ]
            }

### Get Google [GET /api/v1/admin/googles/{google_id}]

+ Parameters
    + `google_id`: 1 (string) - Google Id

+ Request (application/vnd.api+json)

    + Headers

            Authorization:  Bearer <Api Token>

+ Response 200 (application/vnd.api+json)

          {
              "data"=>
                  {
                      "id"=>"42afb9e3-c5bb-4c0a-ac3c-8b4fd388965d",
                      "type"=>"googles",
                      "links"=>{"self"=>"http://www.example.com/api/v1/admin/googles/42afb9e3-c5bb-4c0a-ac3c-8b4fd388965d"},
                      "attributes"=>{"uid"=>"ce3a6cbe-ba6b-4b01-a6d9-b8214ebb63f4"},
                      "relationships"=>
                          {
                              "user"=>
                                  {
                                      "links"=>
                                          {
                                              "self"=>"http://www.example.com/api/v1/admin/googles/42afb9e3-c5bb-4c0a-ac3c-8b4fd388965d/relationships/user",
                                              "related"=>"http://www.example.com/api/v1/admin/googles/42afb9e3-c5bb-4c0a-ac3c-8b4fd388965d/user"
                                          }
                                  }
                              "email"=>
                                  {
                                      "links"=>
                                          {
                                              "self"=>"http://www.example.com/api/v1/admin/googles/42afb9e3-c5bb-4c0a-ac3c-8b4fd388965d/relationships/email",
                                              "related"=>"http://www.example.com/api/v1/admin/googles/42afb9e3-c5bb-4c0a-ac3c-8b4fd388965d/email"
                                          }
                                  }    
                          }
                  }
          }

### Delete Google [DELETE /api/v1/admin/googles/{google_id}]

+ Parameters
    + google_id: 1 (string) - Google Id

+ Request (application/vnd.api+json)

    + Headers

            Authorization:  Bearer <Api Token>

+ Response 204 (application/vnd.api+json)