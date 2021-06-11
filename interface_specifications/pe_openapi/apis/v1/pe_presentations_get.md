
### Verifiable Presentations GET

`GET /exchange/{sessionId}/presentations?offset=0&limit=20`


#### Description

Retrieve all presentations for this exchange session with pagination.

#### Parameters

Path Variables:
* `sessionId`: the session id associated with the interaction
* `offset`: starting-index of the results. This can be overridden by the API side if it is not a practical number.
* `limit`: the number of results required. This can be overridden by the API side if it is not a practical number.

#### Response

* `200`: Success

  Response Body:
    ```json
    [
      {
        "verifiablePresentation": {
          
        },
        "warnings": [
  
        ],
        "errors": [
        
        ]
      }
      
      
    ]
    ```
