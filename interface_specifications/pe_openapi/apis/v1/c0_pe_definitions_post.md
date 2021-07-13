### Presentation Definitions POST

`POST /pe/v1/definitions/`


#### Description

Add/save a Presentation Definitions on the server.


#### Request Body

  ```json
    {
      "thread": {
        "id": "f1ca8245-ab2d-4d9c-8d7d-94bf310314ef"
      },
      "presentation_definition": {
        "id": "32f54163-7166-48f1-93d8-ff217bdb0653"

      },
      "challenge": {
        "holder": "did:example:12345",
        "token": "1e84250c-25a7-444c-a42b-0a8c43d900e6"
      },
      "callback": {
        "url": "https://verifier-example.io/pe/f1ca8245-ab2d-4d9c-8d7d-94bf310314ef/definitions/32f54163-7166-48f1-93d8-ff217bdb0653/status"
      }
    }
  ```

#### Response

* `200`: OK

  Response Body

    ```json
    {
      "definition_url": "https://pe-rest-api-example.io/pe/v1/f1ca8245-ab2d-4d9c-8d7d-94bf310314ef/definitions/32f54163-7166-48f1-93d8-ff217bdb0653/"
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
