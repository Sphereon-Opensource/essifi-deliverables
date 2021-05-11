# Interface Specification for Presentation Exchange REST API

The goal of the REST API for Presentation Exchange is to:

* Expose the functionality of the [PE Library](./interface_specification_of_pe_library_component.md) for use in any language
* Provide stateful interaction mediation between holders and verifiers

<br/>

![image info](./figures/PE_REST_API_sequence.svg)


## API

* [Initiation](#Initiation)
* [Challenge / Presentation Definition retrieval](#challenge-/-Presentation-Definition-retrieval)
* [Presentation Submission](#Presentation-Submission)
* [Status notification to verifier](#Status-notification-to-verifier)
* [Retrieve Presentation Submission](#Retrieve-Presentation-Submission)
* [Status update](#Status-update)
* [Status notification to holder](#Status-notification-to-holder)
* [Status check](#Status-check)


### Initiation

`POST /exchange`


#### Description

Initiate a new Verifier/Holder interaction


#### Parameters

Request Body:
```json
{
  "presentation_definition": {...},
  "challenge": "1e84250c-25a7-444c-a42b-0a8c43d900e6",
  "holder": "did:example:12345",
  "callback": "https://verifier-example.io/status/12345"
}
```


#### Response

* `200`: OK

    Response Body
    
    ```json
    {
      "challengeTokenUrl": "https://pe-rest-api-example.io/exchange/1234"
    }
    ```
* `400`: Invalid request
  
  Response Body
  
  ```json
  {
    "errors": [...]
  }
  ```


### Challenge / Presentation Definition retrieval

`GET /exchange/{sessionId}`


#### Parameters

Path Variables:

* `sessionId`: the session id returned from the `POST /exchange` initiation call


#### Response

* `200`: Success
  
    Response Body
    ```json
    {
      "presentation_definition": {...},
      "callback": "https://pe-rest-api-example.io/exchange/1234/submission",
      "challenge": "1e84250c-25a7-444c-a42b-0a8c43d900e6"
    }
    ```
* `404`: Session not found


### Presentation Submission

`POST /exchange/{sessionId}/submission`


#### Description

Submit a requested presentation


#### Parameters

Path Variables:
* `sessionId`: the session id associated with the interaction
Request Body:
```json
{
  "verifiablePresentation": {
    ...
  },
  "callback": "https://holder-example.io/status/1234"
}
```


#### Response
* `200`: Success
  
    Response body
    ```json
    {
      "warnings": [...]
    }
    ```
* `400`: Invalid Request
  
    Response Body
    ```json
    {
      "warnings": [...],
      "errors": [...]
    }
    ```

### Status notification to verifier

`Put <verifier-example.io>/status/{sessionId}`


#### Description

This is an optional interaction and hence verifier can choose not to implement it. The PE REST Backend invokes an HTTP REST API exposed by the verifier to notify about the status of exchange.


#### Parameters

Path Variables:
* `sessionId`: the session id associated with the interaction

Request Body:
```json
{
  "status": "SUBMITTED"
}
```

#### Response

* `200`: Success


* `202`: Accepted
  Verifier can respond immediately with `202 accepted`, or it can invoke an HTTP API later asynchronously.


* `404`: Exchange session not found


### Retrieve Presentation Submission

`GET /exchange/{sessionId}/submission`


#### Description

Retrieve a presentation submission as a verifier as part of a credential exchange session.


#### Parameters

Path Variables:
* `sessionId`: the session id associated with the interaction
  

#### Response

* `200`: Success
  
  Response Body:
    ```json
    {
      "verifiablePresentation": {
        ...
      },
      "warnings": [...],
      "errors": [...]
    }
    ```
* `404`: Submission not found


### Status update

`Post /exchange/{sessionId}/status`


#### Description

Verifier can update the status from `SUBMITTED` to `ACCEPTED` by calling this API.


#### Parameters

Path Variables:
* `sessionId`: the session id associated with the interaction
  Request Body:
    ```json
    {
      "status": "ACCEPTED",
      "message": "The submission has been accepted without reservation"
    }
    ```


#### Response

* `200`: Success

* `404`: Submission not found


### Status notification to holder

`Put <holder-example.io>/status/{sessionId}`


#### Description

This is an optional interaction and hence holder can choose not to implement it. The PE REST Backend invokes an HTTP REST API exposed by the holder to notify about the status of exchange.

#### Parameters

Path Variables:
* `sessionId`: the session id associated with the interaction

Request Body:
```json
{
  "status": "ACCEPTED"
}
```

#### Response

* `200`: Success


* `404`: Exchange session not found


### Status check

`GET /exchange/{sessionId}/status`


#### Description

Check on the status of an ongoing exchange session


#### Parameters

Path Variables:
* `sessionId`: the session id associated with the interaction


#### Response

* `200`: Success
  
  Response Body
    ```json
    {
      "status": "SUBMITTED"
    }
    ```
  * following can be values for `status`:
      * `CREATED`: create a session http request was successful
      * `SUBMITTED`: Holder responded with a submission
      * `HOLDER_DECLINED`: (holder_refused)Holder explicitly declined, Holder called some API to update the status.
      * `EXPIRED`: Holder did not respond at all or did not respond in time.
      * `ACCEPTED`: (completed/verified/valid/approved) Submission was accepted by the verifier.
      * `VERIFIER_DECLINED`: (verifier_rejected) Submission was rejected by verifier
    
* `404`: Exchange session not found
