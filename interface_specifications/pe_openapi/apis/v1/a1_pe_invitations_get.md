### invitations GET

`GET /pe/v1/invitations/{oobid}`


#### Description

Once a party(e.g. Verifier) has posted an [invitation](a0_pe_invitations_post.md) the receiver(e.g. Holder) can GET the invitations.


#### Parameters

Path Variables:

* `oobid`: out of band message id e.g. `5f0e3ffb-3f92-4648-9868-0d6f8889e6f3`


#### Response

  * `200`: Success
     
    Base 64 URL Encoded:

    ``` 
     eyJ0eXBlIjoiaHR0cHM6Ly9kaWRjb21tLm9yZy9vdXQtb2YtYmFuZC8wLjEvaW52aXRhdGlvbiIsImlkIjoiNjkyMTJhM2EtZDA2OC00ZjlkLWEyZGQtNDc0MWJjYTg5YWYzIiwiZnJvbSI6ImRpZDpleGFtcGxlOmFsaWNlIiwiYm9keSI6eyJnb2FsX2NvZGUiOiIiLCJnb2FsIjogIiIsInJlcXVlc3R
    ```

* `404`: Not found
****