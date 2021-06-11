### Presentation Definition Challenge GET

`GET /exchange/{sessionId}`


#### Parameters

Path Variables:

* `sessionId`: the session id returned from the `POST /exchange` initiation call


#### Response

* `200`: Success

  Response Body
    ```json
    {
        "presentation_definition": {
  
        },
        "challenge": {
          "holder": "did:example:12345",
          "token": "1e84250c-25a7-444c-a42b-0a8c43d900e6"
        }
    }
    ```
* `404`: Session not found

