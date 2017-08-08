## Admin Groups [/api/v1/admin/groups]
###Relations

###has_many
+ users

### Get All Groups [GET /api/v1/admin/groups]

+ Request (application/vnd.api+json)

    + Headers

            Authorization:  Bearer <Api Token>

+ Response 200 (application/vnd.api+json)

            {
                "data"=>
                    [
                        {
                            "id"=>"8fdbcd92-a000-413d-ad65-b5eaf93f539d",
                            "type"=>"groups",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/groups/8fdbcd92-a000-413d-ad65-b5eaf93f539d"},
                            "attributes"=>{"name"=>"hoodie-xoxo-brooklyn"},
                            "relationships"=>
                                {
                                    "users"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/groups/8fdbcd92-a000-413d-ad65-b5eaf93f539d/relationships/users",
                                                    "related"=>"http://www.example.com/api/v1/admin/groups/8fdbcd92-a000-413d-ad65-b5eaf93f539d/users"
                                                }
                                        }
                                }
                        },
                        {
                            "id"=>"fddf36ed-2ca9-4b7a-9db9-e77fff1b737a",
                            "type"=>"groups",
                            "links"=>{"self"=>"http://www.example.com/api/v1/admin/groups/fddf36ed-2ca9-4b7a-9db9-e77fff1b737a"},
                            "attributes"=>{"name"=>"paleo-kickstarter-+1"},
                            "relationships"=>
                                {
                                    "users"=>
                                        {
                                            "links"=>
                                                {
                                                    "self"=>"http://www.example.com/api/v1/admin/groups/fddf36ed-2ca9-4b7a-9db9-e77fff1b737a/relationships/users",
                                                    "related"=>"http://www.example.com/api/v1/admin/groups/fddf36ed-2ca9-4b7a-9db9-e77fff1b737a/users"
                                                }
                                        }
                                }
                        }
                    ]
            }

### Get Group [GET /api/v1/admins/groups/{group_id}]

+ Parameters
    + `group_id`: 1 (string) - Group Id

+ Request (application/vnd.api+json)

     + Headers
    
            Authorization:  Bearer <Api Token>

+ Response 200 (application/vnd.api+json)

            {
                "data"=>
                    {
                        "id"=>"730b05a5-636e-4897-805e-c914e459277e",
                        "type"=>"groups",
                        "links"=>{"self"=>"http://www.example.com/api/v1/admin/groups/730b05a5-636e-4897-805e-c914e459277e"},
                        "attributes"=>{"name"=>"group name"},
                        "relationships"=>
                            {
                                "users"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/groups/730b05a5-636e-4897-805e-c914e459277e/relationships/users",
                                                "related"=>"http://www.example.com/api/v1/admin/groups/730b05a5-636e-4897-805e-c914e459277e/users"
                                            }
                                    }
                            }
                    }
            }

### Create Group [POST]

+ Request (application/vnd.api+json)

     + Headers
    
            Authorization:  Bearer <Api Token>
            
     + Body
      
            {
                "data": 
                    {
                        "type": "access_profiles",
                        "attributes": 
                            {
                               "name": 'group name',
                            },
                    }
            }  

+ Response 201 (application/vnd.api+json)

            {
                "data"=>
                    {
                        "id"=>"730b05a5-636e-4897-805e-c914e459277e",
                        "type"=>"groups",
                        "links"=>{"self"=>"http://www.example.com/api/v1/admin/groups/730b05a5-636e-4897-805e-c914e459277e"},
                        "attributes"=>{"name"=>"group name"},
                        "relationships"=>
                            {
                                "users"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/groups/730b05a5-636e-4897-805e-c914e459277e/relationships/users",
                                                "related"=>"http://www.example.com/api/v1/admin/groups/730b05a5-636e-4897-805e-c914e459277e/users"
                                            }
                                    }
                            }
                    }
            } 

### Update Group [PUT /api/v1/admin/groups/{group_id}]

+ Parameters
    + group_id: 1 (string) - Group Id

+ Request (application/vnd.api+json)

     + Headers

            Authorization:  Bearer <Api Token>
            
     + Body
     
            {
                "data": 
                    {
                        "type": "access_profiles",
                        "attributes": 
                            {
                                "name": 'group name qwe',
                            },
                    }
            }       

+ Response 200 (application/vnd.api+json)

            
            {
                "data"=>
                    {
                        "id"=>"730b05a5-636e-4897-805e-c914e459277e",
                        "type"=>"groups",
                        "links"=>{"self"=>"http://www.example.com/api/v1/admin/groups/730b05a5-636e-4897-805e-c914e459277e"},
                        "attributes"=>{"name"=>"group name qwe"},
                        "relationships"=>
                            {
                                "users"=>
                                    {
                                        "links"=>
                                            {
                                                "self"=>"http://www.example.com/api/v1/admin/groups/730b05a5-636e-4897-805e-c914e459277e/relationships/users",
                                                "related"=>"http://www.example.com/api/v1/admin/groups/730b05a5-636e-4897-805e-c914e459277e/users"
                                            }
                                    }
                            }
                    }
            } 

### Delete Group [DELETE /api/v1/admin/groups/{group_id}]

+ Parameters
    + group_id: 1 (string) - Group Id

+ Request (application/vnd.api+json)

    + Headers
        
            Authorization:  Bearer <Api Token>

+ Response 204 (application/vnd.api+json)