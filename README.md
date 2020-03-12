HOST: https://private-8c9d0c-fayzisme.apiary-mock.com/
# fayzisme API

API documentation for E-commerce 

## Categories Collection [/categories{?page}{?limit}]
### List Categories [GET]

+ Parameters
    + page : 1 (number) - optional
    + limit : 10 (number) - optional


+ Response 200 (application/json)

        {
            "data":[
                {
                    "id": 1,
                    "name": "KAOS",
                    "icon": "kaos.png",
                    "created_at": "2020-03-11T16:29:23.378Z",
                    "updated_at": "2020-03-11T16:29:23.378Z"
                },
                {
                    "id": 2,
                    "name": "KEMEJA",
                    "icon": "kemeja.png",
                    "created_at": "2020-03-11T16:29:23.378Z",
                    "updated_at": "2020-03-11T16:29:23.378Z"
                },
                {
                    "id": 3,
                    "name": "SEPATU",
                    "icon": "sepatu.png",
                    "created_at": "2020-03-11T16:29:23.378Z",
                    "updated_at": "2020-03-11T16:29:23.378Z"
                },
                {
                    "id": 4,
                    "name": "AKSESORIS",
                    "icon": "aksesoris.png",
                    "created_at": "2020-03-11T16:29:23.378Z",
                    "updated_at": "2020-03-11T16:29:23.378Z"
                }
            ],
            "meta": {
                "total": 30,
                "page": 1,
                "limit":10
                
            }
        }


### Create a New Category [POST]

+ Request (application/json)

        {
            "name": "JAKET",
            "icon": "jaket.png"
        }

+ Response 201 (application/json)

    + Headers

            Location: /categories/10

    + Body

            {
            "status": "OK",
            "message": "Successful",
             "data":
                 {
                    "id": 5,
                    "name": "JAKET",
                    "icon": "jaket.png",
                    "created_at": "2020-03-11T16:29:23.378Z",
                    "updated_at": ""
                 }
            }


### Update Category with PUT [PUT /{id}]

+ Parameters
    + id (number) - ID of category must integer

+ Request (application/json)

        {
            "id": 5,
            "name": "JAKET",
            "icon": "jaket.png"
        }

+ Response 204 (application/json)


### Update Category with PATCH [PATCH /{id}]

+ Parameters
    + id (number) - ID of category must integer

+ Request (application/json)

        {
            "name": "JAKET"
        }

+ Response 204 (application/json)


### Detail Category [GET /{id}]

+ Parameters
    + id: 1 (number) - ID of category must integer

+ Response 200 (application/json)

        {
            "name": "KAOS",
            "icon": "kaos.png",
            "created_at": "2020-03-11T15:16:32.671Z",
            "updated_at": "2020-03-11T15:40:32.671Z"
        }

### Delete Category [DELETE /{id}]

+ Parameters
    + id (number) - ID of category must integer

+ Response 204 (application/json)
