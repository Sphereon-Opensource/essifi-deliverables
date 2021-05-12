# Functional Specification for Presentation Exchange Library

Presentation Exchange Library (Typescript) implements core functionality of [DIF Presentation Exchange v1.0.0 specification's](https://identity.foundation/presentation-exchange/) such as:

* validation of the structure of provided presentation definition
* construction of presentation submission from available verifiable credentials
* verification of presentation submissions to be correct as per presentation definition
* Utilities: to build and use different models compliant with the DIF specs.

Sphereon's PE Library is useful for both verifier systems and holders (e.g. wallets) and can be used in client side browsers and mobile applications as well as on server side technology such as REST APIs (e.g. built with NodeJS).

By using the library developers of verifier and holder systems leverage the complete power of DIF specification which offers not only consistency but also standardization across various parts of exchange.

Using PE Library gives more control and insight into DIF components than developers using PE REST API get.