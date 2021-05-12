# Functional Specification for Presentation Exchange Library

Presentation Exchange Library (Typescript) implements core functionality of [DIF Presentation Exchange v1.0.0 specification's](https://identity.foundation/presentation-exchange/).

The verifier creates a Presentation Definition asking for credentials from the holder. The definition for the credentials is sent to the holder, who returns a presentation as a response. Now the verifier will verify the presentation by checking the signature and other accompanying proofs. The presentation exchange will make sure that the model the verifier uses can be understood by the holder and that the correct parts from the holders credentials have been used to create the presentation. The exchange will contain the logic to interpret these models, therefore removing the effort for the verifier and holder to align their specific models.

Sphereon's PE Library is useful for both verifier systems and holders (e.g. wallets) and can be used in client side browsers and mobile applications as well as on server side technology such as REST APIs (e.g. built with NodeJS).

Using PE Library gives more control and insight into DIF components than developers using PE REST API get.