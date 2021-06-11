### Status Notification to Verifier or Holder

`Put <verifier-or-holder-example.io>/exchange/{sessionId}/status`


#### Description

This is an optional interaction and hence party can choose not to implement it. The PE REST Backend invokes an HTTP REST API exposed by the party to notify about the status of exchange.

#### Parameters

Path Variables:
* `sessionId`: the session id associated with the interaction

Request Body ( Example : notification to Holder ):
```json
{
  "presentationId": "presentationId",
  "status": "ACCEPTED",
  "message": "The presentation has been accepted without reservation"
}
```

Request Body ( Example : notification to Verifier ):
```json
{
  "presentationId": "presentationId",
  "status": "SUBMITTED"
}
```

#### Response

* `200`: Success

* `404`: Exchange session not found
