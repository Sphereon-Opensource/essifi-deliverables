### Verifiable Presentation GET

`GET /exchange/{sessionId}/presentations/{presentationId}`


#### Description

Retrieve a presentation as a verifier as part of a credential exchange session.


#### Parameters

Path Variables:
* `sessionId`: the session id associated with the interaction
* `presentationId`: presentationId created when presentation was submitted


#### Response

* `200`: Success

  Response Body:
    ```json
    {
      "verifiablePresentation": {
        
      },
      "warnings": [
  
      ],
      "errors": [
      
      ]
    }
    ```
* `404`: Presentation not found

