
### Presentation Status GET

`GET /pe/v1/{thid}/presentation/{presentation_id}/status`


#### Description

Check on the status of a presentation.


#### Parameters

Path Variables:
* `thid`: Thread ID associated with the presentation exchange. e.g. `f1ca8245-ab2d-4d9c-8d7d-94bf310314ef`
* `presentation_id`: "a30e3b91-fb77-4d22-95fa-871689c322e2"

#### Response

* `200`: Success

  Response Body
    ```json
    {
      "thid": "f1ca8245-ab2d-4d9c-8d7d-94bf310314ef",
      "presentation_id": "a30e3b91-fb77-4d22-95fa-871689c322e2", 
      "status": "SUBMITTED",
      "message": "Some warnings were found"
    }
    ```
    * `status` [Possible Status](../statuses.md)

* `404`: Exchange session not found
