### Presentation Status POST

`POST /pe/v1/presentations/{presentation_id}/statuses`

#### Description

Verifier can update the status from `SUBMITTED` to `ACCEPTED` by calling this API.


#### Parameters

Path Variables:
* `presentation_id`: "a30e3b91-fb77-4d22-95fa-871689c322e2"

  Request Body:
  ```json
  {
    "status": "ACCEPTED",
    "message": "The presentation has been accepted without reservation"
  }
  ```


#### Response

* `200`: Success

  Response Body:

  ```json
  {
    "thread":{
      "id": "f1ca8245-ab2d-4d9c-8d7d-94bf310314ef"
    },
    "presentation_id": "a30e3b91-fb77-4d22-95fa-871689c322e2", 
    "status": "ACCEPTED",
    "message": "The presentation has been accepted without reservation"
  }
  ```

* `404`: Submission not found
