### Status Notification to Holder

`PUT <holder-example.io>pe/presentations/{presentation_id}/statuses`


#### Description

This is an optional interaction and hence party can choose not to implement it. The PE REST Backend invokes an HTTP REST API exposed by the party to notify about the status of exchange.

#### Parameters

Path Variables:
* `presentation_id`: presentation id e.g. `a30e3b91-fb77-4d22-95fa-871689c322e2`

Request Body:
```json
{
  "thread":{
    "id": "f1ca8245-ab2d-4d9c-8d7d-94bf310314ef"
  },
  "presentation_id": "a30e3b91-fb77-4d22-95fa-871689c322e2",
  "status": "ACCEPTED"
}
```

#### Response

* `200`: Success

* `404`: Exchange session not found
