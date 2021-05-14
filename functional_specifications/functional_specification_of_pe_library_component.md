# Functional Specification for Presentation Exchange Library

The Presentation Exchange Library (Typescript) implements core functionality of [DIF Presentation Exchange v1.0.0 specification's](https://identity.foundation/presentation-exchange/).

Sphereon's PE Library is useful for both verifier systems and holders (e.g. wallets) and can be used in client side browsers and mobile applications as well as on server side technology such as REST APIs (e.g. built with NodeJS). By using the library, developers of verifier and holder systems leverage the complete power of DIF specification, which offers not only consistency but also standardization across various parts of an exchange. Using the PE Library gives someone more direct control, integration and customization for PE components than developers using PE REST API does.

The presentation exchange operates generaly as follows; The verifier creates a Presentation Definition asking for credentials from the holder. The definition for the credentials is sent to the holder, who returns a presentation as a response. Now the verifier will verify the presentation by checking the signature and other accompanying proofs. The presentation exchange will ensure that the model used by the verifier, can be interpreted by the holder. It then ensures that the correct parts from the holders credentials are used to create the presentation. The PE contains all the logic to interpret the models, therefore removing the need for the verifier and holder to align their specific models.

The PE Library will (at least) support the following actions:

    - Validation of the structure of the provided presentation definition;
    - Deconstruction of presentation submission(s) from available verifiable credentials;
    - Verification of presentation submissions as per the defined presentation definition;
    - Utilities to build and use different models compliant with the DIF specs.
