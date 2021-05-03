Envisioned interoperability
===========================

Sphereon's eSSIF Infrastructure project focuses on the interaction between holders and verifiers within an SSI ecosystem. We are working from the standardized [DIF Presentation Exchange specification](https://identity.foundation/presentation-exchange/), and using Verifiable Credentials as per the [W3C Data Model](https://www.w3.org/TR/vc-data-model/).

Given the opensource specifications and standards on which our project relies, as well as the common need for holder-verifier interactions in any SSI architecture, we see an abundance of possible interoperability avenues to pursue with members both inside and outside the eSSIF Labs cohort.

### Presentation Exchange API Interop
One fundamental goal in interoperability initiatives is to test the compatibility of independent implementations of the same specification. This lays the groundwork for refinement of specifications and gives a reliable basis for future implementations and adoption of the specification.

From this perspective of interoperability, we see a strong directional alignment between Sphereon's Presentation Exchange API and the [Presentation Exchange working package](https://gitlab.grnet.gr/essif-lab/infrastructure_2/gataca/Verifier_Universal_Interface/-/tree/master/WP1-PresentationExchange) of Gataca's Verifier Universal Interface initiative (VUI). Sphereon's participation in the working package would enable both better refinement and compatibility of our own Presentation Exchange REST API interface, as well as contribute to the VUI goals regarding multiple independent implementations.

Beyond the interface compatibility of Sphereon's PE REST API, we would also seek to demonstrate mutual interoperability of the underlying Presentation Exchange specification logic as part of the VUI work package. This would involve participation and collaboration in writing test suites and designing protocols that can probe the underlying presentation request and credential query logic implemented in our Presentation Exchange Library, which would result in a technical validation of the DIF presentation exchange spec and potentially enable us to propose further refinements.

The PE REST API interop as part of the VUI work package would involve initial independent implementations by Sphereon and Gataca, but could later be expanded by any member willing to provide further implementations. 

### Wallet Compatibility

Another aspect of interoperability that Sphereon is looking to target within the scope of the eSSIF-Labs infrastructure project regarding wallet compatibility. Our Presentation Exchange API serves as a mediator between verifiers who are seeking to verify certain credentials, and holders who hold those credentials (where verifiers and holders are interchangeable amongst parties in a symmetric relationship). This type of negotiation is reliant on some form of VC wallet that recognizes the data types and objects associated with the exchange, and is compatible with the protocol for negotiating Presentation Exchange.

Given our conformance to the DIF Presentation Exchange specification, and our planning involvement in the Verifier Universal Interface, the goal of wallet compatibility is not just a matter of integration, but rather of interoperability and conformance to a set of specifications and protocols. We would start by targeting wallet implementations that already use Verifiable Credentials as per the W3C Data model, and eventually move on to compatibility with wallets that conform to Hyperledger Aries protocols, particularly the Aries Present-Proof 2.0 protocol, which already supports DIF Presentation Exchange objects.

Within eSSIF-Labs, some of the companies that we would target for potential wallet-compatibility interoperability efforts would include:
* Jolocom
* LetsTrust
* Gimly

### Beyond eSSIF Labs

One of the eventual goals of our project is to bridge the gap between the W3C-CCG specifications (such as the VC-HTTP-API) and the Hyperledger Aries specifications/implementations. For this purpose, a new work item has been created within the DIF Claims and Credentials working group. This will involve collaboration with representatives in a broad range of SSI spaces (DIF/W3C-CCG/Aries) who seek to define a new test suite and extend/adapt existing specifications and protocols in W3C and Aries to enable compatibility and standardization around verifier/holder interactions.

Sphereon's participation in the group would enable us to broaden the target audience of eSSIF Labs interoperability efforts, and provide a channel for communication and alignment between internal eSSIF Lab members and the broader SSI community.

