### Status Notification to Verifier

`PUT <verifier-example.io>pe/definitions/{definition_id}/statuses`


#### Description

This is an optional interaction and hence party can choose not to implement it. The PE REST Backend invokes an HTTP REST API exposed by the party to notify about the status of exchange.

#### Parameters

Path Variables:
* `definition_id`: definition id e.g. `32f54163-7166-48f1-93d8-ff217bdb0653`

Request Body

```json
{
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

#### See also : [Possible Status](../statuses.md)
