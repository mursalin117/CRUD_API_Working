FORMAT: 1A
HOST: http://localhost:8000/

# campus-api

This is a restful api for finding any information about the users. If 
someone wants to get some information about any person, he/she can easily 
check here.

## Users Information [/campus/user]

All the list of user and their informations can be got here.

### List All Users [GET]

This action will show this list of the users and their informations which 
are contained by the database.

+ Response 200 (application/json)

        [
            {
                "id": "1",
                "Name": "Nahid",
                "ID": "139"
            },
            {
                "id": "2",
                "Name": "Rafi",
                "ID": "106"
            },
            {
                "id": "3",
                "Name": "Rakib",
                "ID": "111"
            }
        ]

### Add a New User [POST]

One can easily add his information in listvusing the following - 
1. Name    
2. ID

For adding the new User the POST method is implemented.

+ Request (application/json)

        {
            "Name": "Shaon",
            "ID": "120"
        }

+ Response 201 (application/json)

    + Headers

            Location: /campus/user/4

    + Body

            {
                "id": "4",
                "Name": "Shaon",
                "ID": "120"
            }

### Update a User’s Information [PUT]

One can change his information here. For this action, the PUT method 
is implemented. This will update information in database.

+ Request (application/json)

        {
                "Name": "Shaon",
                "ID": "127"
        }

+ Response 201 (application/json)

    + Headers

            Location: /campus/user/4

    + Body

            {
                "id": "4",
                "Name": "Shaon",
                "ID": "127"
            }

### Remove a User [DELETE]

One can remove his information from the database using the DELETE method 
which will remove the user and his information from the list.


+ Request (application/json)

        {
            "Name": "Shaon",
            "ID": "127"
        }

+ Response 201 (application/json)

    + Headers

            Location: /campus/user/4

    + Body

            {
                "message": "Product deleted successfully!"
            }
