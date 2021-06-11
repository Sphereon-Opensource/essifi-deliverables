### Presentation POST

`POST /exchange/{sessionId}/presentations`


#### Description

Submit a requested presentation


#### Parameters

Path Variables:
* `sessionId`: the session id associated with the interaction


Request Body:
  ```json
  {
    "verifiablePresentation": {
      
    },
    "callback": {
      "url": "https://holder-example.io/status/1234"
    }
  }
  ```


#### Response
* `200`: Success

  Response body
    ```json
    {
      "presentationId": "presentationId", 
      "warnings": [
  
      ]
    }
    ```

* `400`: Invalid Request

  Response Body
    ```json
    {
      "warnings": [
      
      ],
      "errors": [
      
      ]
    }
    ```
