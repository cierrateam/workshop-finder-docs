---
title: API Reference

language_tabs:
- bash

includes:

search: true

toc_footers:
- <a href='http://github.com/mpociot/documentarian'>Documentation Powered by Documentarian</a>
---
<!-- START_INFO -->
# Info

Welcome to the generated API reference. All the endpoints are reachable without auth.

<!-- END_INFO -->

#api


<!-- START_2b6e5a4b188cb183c7e59558cce36cb6 -->
## Get the currently logged in user


> No example provided.

### HTTP Request
`GET api/user`

### Query Parameters

Key | Description
--------- | -----------


<!-- END_2b6e5a4b188cb183c7e59558cce36cb6 -->

<!-- START_d0be1483d167d9342fb319522d271621 -->
## List workshops

List all workshops around a specific user location.

> List workshops :

```bash
curl -X GET -G "http://workshop-finder-api.test/api/workshops?lat=51.5265529&amp;lng=9.9023838&amp;radius=150000" \

```


> Example response (200) :

```json
{
    "data": [
        {
            "id": 2,
            "company_name": "cierra GmbH",
            "lat": "51.5265529",
            "lng": "9.9023838",
            "note": "This is an example note to the company cierra. Write something interesting here.",
            "address": "Bachstraße 2, 37081 Göttingen",
            "telefon": "055189999000",
            "email": "support@cierra.de",
            "created_at": "2020-05-06T19:06:58.000000Z",
            "updated_at": "2020-05-06T19:06:58.000000Z"
        },
        {
            "id": 1,
            "company_name": "cierra GmbH",
            "lat": "51.5265529",
            "lng": "9.9023838",
            "note": "This is an example note to the company cierra. Write something interesting here.",
            "address": "Bachstraße 2, 37081 Göttingen",
            "telefon": "055189999000",
            "email": "support@cierra.de",
            "created_at": "2020-05-06T19:00:10.000000Z",
            "updated_at": "2020-05-06T19:00:10.000000Z"
        }
    ]
}
```

### HTTP Request
`GET api/workshops`

### Query Parameters

Key | Description
--------- | -----------
lat | REQUIRED
lng | REQUIRED
radius | In meters. Default 150000


<!-- END_d0be1483d167d9342fb319522d271621 -->

<!-- START_935d4f17608b589a4380b70e7380c715 -->
## Create Workshop

> Create Workshop :

```bash
curl -X POST "http://workshop-finder-api.test/api/workshops" \
    -H "Content-Type: application/x-www-form-urlencoded" \
    -H "Accept: application/json" \

```


> Example response (200) :

```json
{
    "message": "Created Workshop",
    "data": {
        "company_name": "cierra GmbH",
        "lat": "51.5265529",
        "lng": "9.9023838",
        "note": "This is an example note to the company cierra. Write something interesting here.",
        "address": "Bachstraße 2, 37081 Göttingen",
        "telefon": "055189999000",
        "email": "support@cierra.de",
        "updated_at": "2020-05-06T19:06:58.000000Z",
        "created_at": "2020-05-06T19:06:58.000000Z",
        "id": 2
    }
}
```

### HTTP Request
`POST api/workshops`

### Query Parameters

Key | Description
--------- | -----------

### Body Parameters

Key | Description
--------- | -----------
company_name | REQUIRED - The name of the workshop
lat | REQUIRED - The latitude of the workshop
lng | REQUIRED - The longitude of the workshop
note | A freetext description of the workshop.
address | REQUIRED - The postaddress of the workshop.
telefon | Phone number of the workshop
email | The email address of the company.

<!-- END_935d4f17608b589a4380b70e7380c715 -->

<!-- START_b87225e7834b5533e524be98e27527fc -->
## Get workshop details


> No example provided.

### HTTP Request
`GET api/workshops/{workshop}`

### Query Parameters

Key | Description
--------- | -----------


<!-- END_b87225e7834b5533e524be98e27527fc -->

<!-- START_6ccfac82cc098e7d4db50ff88ba24547 -->
## Update workshop


> No example provided.

### HTTP Request
`PUT api/workshops/{workshop}`
`PATCH api/workshops/{workshop}`

### Query Parameters

Key | Description
--------- | -----------


<!-- END_6ccfac82cc098e7d4db50ff88ba24547 -->

<!-- START_7a9342c92fdadc43a81470f827447aff -->
## Delete a workshop


> No example provided.

### HTTP Request
`DELETE api/workshops/{workshop}`

### Query Parameters

Key | Description
--------- | -----------


<!-- END_7a9342c92fdadc43a81470f827447aff -->


