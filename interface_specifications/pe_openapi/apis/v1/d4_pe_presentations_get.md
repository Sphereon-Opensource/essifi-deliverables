### Presentations GET

`GET /pe/v1/{thid}/presentations?offset=0&limit=20`


#### Description

Retrieve all presentations for this exchange session with pagination.

#### Parameters

Path Variables:
* `thid`: Thread ID associated with the presentation exchange. e.g. `f1ca8245-ab2d-4d9c-8d7d-94bf310314ef`
* `offset`: starting-index of the results. This can be overridden by the API side if it is not a practical number.
* `limit`: the number of results required. This can be overridden by the API side if it is not a practical number.

#### Response

* `200`: Success

  Response Body:
```json
  {
    "presentations": [
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
    ]
  }
```
* `404`: Presentation not found
