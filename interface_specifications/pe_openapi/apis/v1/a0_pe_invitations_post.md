### invitations POST

`POST /pe/v1/invitations/`


#### Description

A party (usually Verifier) can provide information (to holders) to connect (to verifier) on a web page. The recipient (e.g. holder) will visit the web page and scan a QR Code. This connection invitation can be seen as an out-of-band message.

The receiver (e.g. holder) responds back with its connection detail.

This call creates that invitation to show on the web page.

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
            "from": "DID-A"
          }
        }
      }
    ]
  }
  ```

#### Response

* `200`: Success
    
Send the DIDComm message to the recipient visiting our web page.

```json
  {
    "url": "example.com/pe/v1/invitations/5f0e3ffb-3f92-4648-9868-0d6f8889e6f3"
  }
```

* `404`: Not found


The response can be forwarded to the receiver (e.g. Holder) by party (e.g. Verifier) with additional context as well.

    Dear Holder,
    
    To connect with Verifier-A, click here to [connect](example.com/pe/v1/invitations/5f0e3ffb-3f92-4648-9868-0d6f8889e6f3) with us.
    
    If you don't have an identity agent for holding credentials, you will be given instructions on how you can get one.

