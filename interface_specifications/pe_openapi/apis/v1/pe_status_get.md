
### Status GET

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
      "presentationId": "presentationId", 
      "status": "SUBMITTED",
      "message": "Some warnings were found"
    }
    ```
    * `status` can contain the following values:
        * `CREATED`: create a session http request was successful
        * `SUBMITTED`: Holder responded with a presentation
        * `HOLDER_DECLINED`: (holder_refused)Holder explicitly declined, Holder called some API to update the status.
        * `EXPIRED`: Holder did not respond at all or did not respond in time.
        * `ACCEPTED`: (completed/verified/valid/approved) Presentation was accepted by the verifier.
        * `VERIFIER_DECLINED`: (verifier_rejected) Presentation was rejected by verifier

* `404`: Exchange session not found
