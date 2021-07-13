### invitations POST

`POST /pe/v1/invitations/`


#### Description

Any party (i.e. Verifier or Holder) can request to connect to other party. This connection invitation is sent as an out-of-band message since the DID of others may not be known at this stage.

REST API acts as mediator and forwards the message to the receiver and responds back with the DID of the receiver in a DIDComm message.


#### Request Body:
  ```json  
  {
    "@type": "https://didcomm.org/out-of-band/v1/invitations",
    "@id": "fcc9e41c-4a6d-4007-9116-ae679610d6fb",
    "goal_code": "didcomm_connect",
    "goal": "To connect and issue the did for communication",
    "request~attach": [
      {
        "@id": "request-0",
        "mime-type": "application/json",
        "data": {
          "json": {
            "invitee": "e.g. holder 'B'",
            "from": "DID-A"
          }
        }
      }
    ]
  }
  ```

#### Response

  * `200`: Success
    
    Send the didcomm message to the initiating party.

    ```json
    {
        "url": "example.com/pe/v1/invitations/5f0e3ffb-3f92-4648-9868-0d6f8889e6f3"
    }
    ```

* `404`: Not found


The response will be forwarded to the receiver (e.g. Holder) by party (e.g. Verifier) with additional context.

    Dear Holder,
    
    To connect with Verifier-A, click here to [connect](example.com/pe/v1/invitations/5f0e3ffb-3f92-4648-9868-0d6f8889e6f3) with us.
    
    If you don't have an identity agent for holding credentials, you will be given instructions on how you can get one.

