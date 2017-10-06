## Admin Users [/api/v1/admin/users]
###Relations

###has_many
+ emails
+ facebooks
+ googles
+ groups


### Get All Groups [GET /api/v1/admin/users]

+ Request (application/vnd.api+json)

    + Headers

            Authorization:  Bearer <Api Token>

+ Response 200 (application/vnd.api+json)

            {
                "data"=>
                    [
                        {
                            "id"=>"8fdbcd92-a000-413d-ad65-b5eaf93f539d",
                            "type"=>"users",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/users/8fdbcd92-a000-413d-ad65-b5eaf93f539d"},
                            "attributes"=>{"full-name"=>"Darth Vader"},
                            "relationships"=>
                                {
                                    "emails"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/emails",
                                                    "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/emails"
                                                }
                                        },
                                    "facebooks"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/facebooks",
                                                    "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/facebooks"
                                                }
                                        },
                                    "googles"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/users/b3cae3e3-23e7-4ab4-b061-e4d55491d573/relationships/googles",
                                                    "related"=>"http://www.example.com/api/v1/admin/users/b3cae3e3-23e7-4ab4-b061-e4d55491d573/googles"
                                                }
                                        },            
                                    "groups"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/groups",
                                                    "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/groups"
                                                }
                                        }
                                }
                            
                        },
                        {
                            "id"=>"730b05a5-636e-4897-805e-c914e459277e",
                            "type"=>"users",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/users/730b05a5-636e-4897-805e-c914e459277e"},
                            "attributes"=>{"full-name"=>"Obi Van Kenobi"},
                            "relationships"=>
                                {
                                    "emails"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/emails",
                                                    "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/emails"
                                                }
                                        },
                                    "facebooks"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/facebooks",
                                                    "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/facebooks"
                                                }
                                        },
                                    "googles"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/users/b3cae3e3-23e7-4ab4-b061-e4d55491d573/relationships/googles",
                                                    "related"=>"http://www.example.com/api/v1/admin/users/b3cae3e3-23e7-4ab4-b061-e4d55491d573/googles"
                                                }
                                        },            
                                    "groups"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/groups",
                                                    "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/groups"
                                                }
                                        }
                                }
                        }
                    ]
            }

### Get User [GET /api/v1/admins/users/{user_id}]

+ Parameters
    + `user_id`: 1 (string) - User Id

+ Request (application/vnd.api+json)

     + Headers
    
            Authorization:  Bearer <Api Token>

+ Response 200 (application/vnd.api+json)

            {
                "data"=>
                    {
                        "id"=>"8fdbcd92-a000-413d-ad65-b5eaf93f539d",
                        "type"=>"users",
                        "links"=>{"self"=>"http://www.example.com/api/v1/admin/users/8fdbcd92-a000-413d-ad65-b5eaf93f539d"},
                        "attributes"=>{"full-name"=>"Darth Vader"},
                        "relationships"=>
                            {
                                "emails"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/emails",
                                                "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/emails"
                                            }
                                    },
                                "facebooks"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/facebooks",
                                                "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/facebooks"
                                            }
                                    },
                                "googles"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/users/b3cae3e3-23e7-4ab4-b061-e4d55491d573/relationships/googles",
                                                "related"=>"http://www.example.com/api/v1/admin/users/b3cae3e3-23e7-4ab4-b061-e4d55491d573/googles"
                                            }
                                    },            
                                "groups"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/groups",
                                                "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/groups"
                                            }
                                    }
                            }
                        
                    },
            }

### Create User [POST]

+ Request (application/vnd.api+json)

     + Headers
    
            Authorization:  Bearer <Api Token>
            
     + Body
      
            {
                "data": 
                    {
                        "type": "users",
                        "attributes": 
                            {
                               "full-name": 'Ded Moroz',
                            },
                    }
            }  

+ Response 201 (application/vnd.api+json)

            {
                "data"=>
                    {
                        "id"=>"8fdbcd92-a000-413d-ad65-b5eaf93f539d",
                        "type"=>"users",
                        "links"=>{"self"=>"http://www.example.com/api/v1/admin/users/8fdbcd92-a000-413d-ad65-b5eaf93f539d"},
                        "attributes"=>{"full-name"=>"Ded Moroz"},
                        "relationships"=>
                            {
                                "emails"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/emails",
                                                "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/emails"
                                            }
                                    },
                                "facebooks"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/facebooks",
                                                "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/facebooks"
                                            }
                                    },
                                "googles"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/users/b3cae3e3-23e7-4ab4-b061-e4d55491d573/relationships/googles",
                                                "related"=>"http://www.example.com/api/v1/admin/users/b3cae3e3-23e7-4ab4-b061-e4d55491d573/googles"
                                            }
                                    },            
                                "groups"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/groups",
                                                "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/groups"
                                            }
                                    }
                            }
                        
                    },
            }

### Update Users [PUT /api/v1/admin/users/{user_id}]

+ Parameters
    + user_id: 1 (string) - User Id

+ Request (application/vnd.api+json)

     + Headers

            Authorization:  Bearer <Api Token>
            
     + Body
     
            {
                "data": 
                    {
                        "type": "users",
                        "attributes": 
                            {
                                "full-name": 'Alucard Dracula',
                            },
                    }
            }       

+ Response 200 (application/vnd.api+json)

            
            {
                "data"=>
                    {
                        "id"=>"8fdbcd92-a000-413d-ad65-b5eaf93f539d",
                        "type"=>"users",
                        "links"=>{"self"=>"http://www.example.com/api/v1/admin/users/8fdbcd92-a000-413d-ad65-b5eaf93f539d"},
                        "attributes"=>{"full-name"=>"Alucard Dracula"},
                        "relationships"=>
                            {
                                "emails"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/emails",
                                                "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/emails"
                                            }
                                    },
                                "facebooks"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/facebooks",
                                                "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/facebooks"
                                            }
                                    },
                                "googles"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/users/b3cae3e3-23e7-4ab4-b061-e4d55491d573/relationships/googles",
                                                "related"=>"http://www.example.com/api/v1/admin/users/b3cae3e3-23e7-4ab4-b061-e4d55491d573/googles"
                                            }
                                    },            
                                "groups"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/relationships/groups",
                                                "related"=>"http://www.example.com/api/v1/admin/users/49879d9c-1c01-4811-843a-5f48e0fe9e10/groups"
                                            }
                                    }
                            }
                        
                    },
            }

### Delete User [DELETE /api/v1/admin/users/{user_id}]

+ Parameters
    + user_id: 1 (string) - User Id

+ Request (application/vnd.api+json)

    + Headers
        
            Authorization:  Bearer <Api Token>

+ Response 204 (application/vnd.api+json)