### Presentation Definition GET

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
```
* `404`: Presentation exchange thread not found

