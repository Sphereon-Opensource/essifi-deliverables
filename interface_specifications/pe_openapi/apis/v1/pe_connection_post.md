### Connection POST

`POST /pe/v1/connection/`


#### Description

Once party (e.g. Holder) receives the invitation. The party can send the connection information (i.e. DID)..


#### Request Body:
  ```json  
  {
    "@type": "https://didcomm.org/out-of-band/v1/invitation",
    "@id": "1cd8c62b-d07f-4f35-a92a-8e1453e6fa89",
    "goal_code": "connect",
    "goal": "To connect and issue the did for communication",
    "pthid": "fcc9e41c-4a6d-4007-9116-ae679610d6fb",
    "request~attach": [
      {
        "@id": "response-0",
        "mime-type": "application/json",
        "data": {
          "json": {
            "invitee": "DID-B",
            "for": "DID-A"
        }
      }
    ]
  }
  ```

#### Response

* `200`: Success

* `404`: Not found
