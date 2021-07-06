### Presentation GET

`GET /pe/v1/{thid}/presentation/{presentation_id}`


#### Description

Retrieve a presentation as a verifier as part of a credential exchange session.


#### Parameters

Path Variables:
* `thid`: Thread ID of the presentation exchange thread e.g. `f1ca8245-ab2d-4d9c-8d7d-94bf310314ef`
* `presentation_id`: Presentation ID of submitted presentation e.g. `a30e3b91-fb77-4d22-95fa-871689c322e2`


#### Response

* `200`: Success

  Response Body:
```json
  {
    "presentation_submission": {
      "id": "a30e3b91-fb77-4d22-95fa-871689c322e2",
      "definition_id": "32f54163-7166-48f1-93d8-ff217bdb0653",
      "descriptor_map": [
        {
          "id": "banking_input_2",
          "format": "jwt_vc",
          "path": "$.verifiableCredential[0]"
        },
        {
          "id": "employment_input",
          "format": "ldp_vc",
          "path": "$.verifiableCredential[1]"
        },
        {
          "id": "citizenship_input_1",
          "format": "ldp_vc",
          "path": "$.verifiableCredential[2]"
        }
      ]
    },
    "challenge": {
      "token": "1e84250c-25a7-444c-a42b-0a8c43d900e6"
    },
    "callback": {
      "url": "https://holder-example.io/pe/f1ca8245-ab2d-4d9c-8d7d-94bf310314ef/presentation/a30e3b91-fb77-4d22-95fa-871689c322e2"
    }
  }
```
* `404`: Presentation not found

