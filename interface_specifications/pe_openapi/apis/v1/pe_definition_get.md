### Presentation Definition Challenge GET

`GET /pe/v1/{thid}/definition/{definition_id}`


#### Parameters

Path Variables:

* `thid`: Thread ID associated with the presentation exchange. e.g. `f1ca8245-ab2d-4d9c-8d7d-94bf310314ef`
* `definition_id`: definition_id returned from the previous http request `POST /pe/v1/definition/`. e.g. `32f54163-7166-48f1-93d8-ff217bdb0653`


#### Response

* `200`: Success

  Response Body
    ```json
    {
      "@type": "https://didcomm.org/present-proof/v1/definition",
      "@id": "35295850-7543-41d7-8b08-f8aee5c577de",    
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
                "url":"https://verifier-example.io/f1ca8245-ab2d-4d9c-8d7d-94bf310314ef/status"
              }
            }
          }
        }
      ]
    }
    ```
* `404`: Presentation exchange thread not found

