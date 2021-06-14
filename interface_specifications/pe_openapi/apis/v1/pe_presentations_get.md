
### Verifiable Presentations GET

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
          "@type": "https://didcomm.org/present-proof/v1/presentation",
          "@id": "0133d5d5-31e0-4cff-9e68-e411beedd35b",
          "thid": "f1ca8245-ab2d-4d9c-8d7d-94bf310314ef",
          "comment": "some comment",
          "formats": [
            {
              "attach_id": "5ad3822d-0382-4a40-a5c7-1b35dac02aea",
              "format": "dif/presentation-exchange/submission@v1.0"
            }
          ],
          "presentations~attach": [
            {
              "@id": "5ad3822d-0382-4a40-a5c7-1b35dac02aea",
              "mime-type": "application/ld+json",
              "data": {
                "json": {
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
                  "callback": {
                    "url": "https://holder-example.io/pe/f1ca8245-ab2d-4d9c-8d7d-94bf310314ef/presentation/a30e3b91-fb77-4d22-95fa-871689c322e2"
                  }
                }
              }
            }
          ]
        }
      ]
    }
  ```
* `404`: Presentation not found
