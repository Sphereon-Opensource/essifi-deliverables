### Status Notification to Holder

`PUT <verifier-example.io>pe/{thid}/definition/{definition_id}/status`


#### Description

This is an optional interaction and hence party can choose not to implement it. The PE REST Backend invokes an HTTP REST API exposed by the party to notify about the status of exchange.

#### Parameters

Path Variables:
* `thid`: Thread ID e.g. `f1ca8245-ab2d-4d9c-8d7d-94bf310314ef`
* `definition_id`: definition id e.g. `32f54163-7166-48f1-93d8-ff217bdb0653`

Request Body ( Example : notification to Verifier ):

```json
{
  "thid": "f1ca8245-ab2d-4d9c-8d7d-94bf310314ef",
  "definition_id": "32f54163-7166-48f1-93d8-ff217bdb0653",
  "statuses": [
    {
      "presentation_id": "a30e3b91-fb77-4d22-95fa-871689c322e2",
      "status": "SUBMITTED"
    }
  ]
}
```

#### Response

* `200`: Success

* `404`: Exchange session not found
