### Presentation Definition POST

`POST /pe/v1/{thid}/definition/`


#### Description

Add/save a Presentation Definition on the server.


#### Path Variables:

* `thid`: id returned from the previous http request `POST /pe/v1/` e.g. `f1ca8245-ab2d-4d9c-8d7d-94bf310314ef`


#### Request Body

  ```json
    {
      "@type": "https://didcomm.org/present-proof/v1/definition",
      "@id": "fd3f16c2-9975-4612-80c9-627f6223ea76",
      "thid": "f1ca8245-ab2d-4d9c-8d7d-94bf310314ef",
      "from": "did:example:verifier",
      "to": ["did:example:holder"],
      "comment": "This is didcomm message",
      "formats": [
        {
          "attach_id": "2a3f1c4c-623c-44e6-b159-179048c51260",
          "format": "dif/presentation-exchange/definition@v1.0"
        }
      ],
      "presentations~attach": [
        {
          "@id": "2a3f1c4c-623c-44e6-b159-179048c51260",
          "mime-type": "application/ld+json",
          "data": {
            "json": {
              "presentation_definition": {
                "id": "32f54163-7166-48f1-93d8-ff217bdb0653"
    
              },
              "challenge": {
                "holder": "did:example:12345",
                "token": "1e84250c-25a7-444c-a42b-0a8c43d900e6"
              },
              "callback": {
                "url": "https://verifier-example.io/pe/f1ca8245-ab2d-4d9c-8d7d-94bf310314ef/definition/32f54163-7166-48f1-93d8-ff217bdb0653/status"
              }
            }
          }
        }
      ]
    }
  ```

#### Response

* `200`: OK

  Response Body

    ```json
    {
      "thread_url": "https://pe-rest-api-example.io/pe/v1/f1ca8245-ab2d-4d9c-8d7d-94bf310314ef/definition/32f54163-7166-48f1-93d8-ff217bdb0653/"
    }
    ```

* `400`: Invalid request

  Response Body

  ```json
  {
    "errors": [
    
    ]
  }
  ```
