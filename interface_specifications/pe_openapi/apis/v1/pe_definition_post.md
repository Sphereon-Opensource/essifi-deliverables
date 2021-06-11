### Presentation Definition POST

`POST /exchange`


#### Description

Initiate a new Verifier/Holder interaction by creating a Presentation Definition.


#### Parameters

Request Body:
  ```json
  {
            "presentation_definition": {
              
            },
            "challenge": {
              "holder": "did:example:12345",
              "token": "1e84250c-25a7-444c-a42b-0a8c43d900e6"
            },
            "callback": {
    "url":"https://verifier-example.io/status/12345"
          }
        }
  ```


#### Response

* `200`: OK

  Response Body

    ```json
    {
      "sessionUrl": "https://pe-rest-api-example.io/exchange/1234"
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
