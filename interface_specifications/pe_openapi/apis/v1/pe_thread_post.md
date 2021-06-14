### Presentation Definition POST

`POST /pe/v1/`


#### Description

Initiate a new Verifier/Holder thread on the server. This interaction will be given a ThreadID. This thread id can be used to get to this definition as well as will be used to find other interaction regarding this presentation exchange e.g. presentations of proofs (submissions).


#### Response

* `200`: OK

  Response Body

    ```json
    {
      "thid": "f1ca8245-ab2d-4d9c-8d7d-94bf310314ef"
    }
    ```
