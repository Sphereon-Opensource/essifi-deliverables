### Presentation Definition Status GET

`GET /pe/v1/{thid}/definition/{definition_id}/status`


#### Description

This is an optional interaction and hence party can choose not to implement it.


#### Parameters

Path Variables:
* `thid`: Thread ID e.g. `f1ca8245-ab2d-4d9c-8d7d-94bf310314ef`
* `definition_id`: definition id e.g. `32f54163-7166-48f1-93d8-ff217bdb0653`

Request Body

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

#### See also : [Possible Status](../statuses.md)
