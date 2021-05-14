Envisioned interoperability
===========================

Sphereon's eSSIF-Labs Infrastructure project focuses on the interaction between holders and verifiers within an SSI ecosystem. We are working from the standardized [DIF Presentation Exchange specification](https://identity.foundation/presentation-exchange/), and using Verifiable Credentials as per the [W3C Data Model](https://www.w3.org/TR/vc-data-model/).

Given the open-source specifications and standards on which our project relies, as well as the common need for holder-verifier interactions in any SSI architecture, we see an abundance of possible interoperability avenues to pursue with members both inside and outside the eSSIF-Labs cohort.

### Presentation Exchange API Interoperability
One fundamental goal in interoperability initiatives is to test the compatibility of independent implementations of the same specification. This lays the groundwork for refinement of specifications and gives a reliable basis for future implementations and adoption of the specification.

From this perspective of interoperability, we see a strong directional alignment between Sphereon's Presentation Exchange API and the [Presentation Exchange working package](https://gitlab.grnet.gr/essif-lab/infrastructure_2/gataca/Verifier_Universal_Interface/-/tree/master/WP1-PresentationExchange) of Gataca's Verifier Universal Interface initiative (VUI). Sphereon's participation in the working package would enable both better refinement and compatibility of our own Presentation Exchange REST API interface, as well as contribute to the VUI goals regarding multiple independent implementations.

Beyond the interface compatibility of Sphereon's PE REST API, we also seek to demonstrate mutual interoperability of the underlying Presentation Exchange specification logic as part of the VUI work package. This would involve participation and collaboration in writing test suites and designing protocols that can probe the underlying presentation request and credential query logic implemented in both Presentation Exchange Libraries. This effort should result in a technical validation of the DIF presentation exchange specification, and potentially enable us to propose further refinements.

The PE REST API interop as part of the VUI work package would involve initial independent implementations by Sphereon and Gataca, but could later be expanded by any member willing to provide further implementations. 

### Wallet Compatibility

Another aspect of interoperability that Sphereon is looking to target within the scope of the eSSIF-Labs infrastructure project regards wallet compatibility. The Presentation Exchange API that will be created serves as a mediator between verifiers who are seeking to verify certain credentials, and holders who hold those credentials (where verifiers and holders are interchangeable amongst parties in a symmetric relationship). This type of negotiation is reliant on some form of VC wallet that recognizes the data types and objects associated with the exchange, and is compatible with the protocol for negotiating Presentation Exchange.

Given the conformance to the DIF Presentation Exchange specification, and our planned involvement in the Verifier Universal Interface, the goal of wallet compatibility is not just a matter of integration, but rather of interoperability and conformance to a set of specifications and protocols. We would start by targeting wallet implementations that already use Verifiable Credentials as per the W3C Data model, and eventually move on to compatibility with wallets that conform to Hyperledger Aries protocols, particularly the Aries Present-Proof 2.0 protocol, which already supports DIF Presentation Exchange objects.

Within eSSIF-Labs, some of the companies that we would target for potential wallet-compatibility interoperability efforts would include:
* Jolocom
* LetsTrust
* Gimly

### CHAPI Compatibility

The Credential Handler API is about handling credential requests and credential storage on behalf of the user. The specification defines a number of new Web platform features to handle credential requests and credential storage. We are currently exploring with eSSIF-Labs' LetsTrust how they can leverage our Presentation Exchange and CHAPI integration. This is however still in an early phase.

### Overview of Interoperability Opportunities

As discussed in the previous parts, we have started to define validations of the interoperability of our components together with [other eSSIF groups](https://gitlab.grnet.gr/essif-lab/essif-lab/-/blob/master/infrastructure-call/README.md). Apart from the discussed options, there will be more opportunities to show interoperability. Below is a list of the projects that have been identified to have high interoperability potential. The goal is to get/keep contact with these projects to execute interoperability efforts over the course of the project.

Projects with potential interoperability cases from the eSSIF-Labs Infrastructure call 2 group:
* [Gataca](https://gitlab.grnet.gr/essif-lab/infrastructure_2/gataca/Verifier_Universal_Interface_project_summary) - The projects are quite similar as we are both creating a Presentation Exchange (albeit their initial proposal deviated from DIF's PE), interoperability will be shown by creating a test suite that can be used on both implementations, to verify the correctness against the DIF specification and to show interoperability.
* [LetsTrust](https://gitlab.grnet.gr/essif-lab/infrastructure_2/letstrust/letstrust_project_summary) - Interoperability can be shown by using CHAPI to exchange credentials with their wallet using the PE that is being created.
* [Gimly](https://gitlab.grnet.gr/essif-lab/infrastructure_2/gimly/SSI_NFC_Bridge_project_summary) - Interoperability/integration with their mobile wallet app probably using our lower level libraries.
* [IGrant.IO](https://gitlab.grnet.gr/essif-lab/infrastructure_2/igrantio/Automated_Data_Agreements_project_summary) - The consent mechanism they are building can be potentially be included with our PE. Note that the consent mechanism is also part of the Gataca universal interface.
* [Danube Tech](https://gitlab.grnet.gr/essif-lab/infrastructure_2/danubetech/SSI_Java_Libraries_project_summary) - They could use the created OpenAPI specification to generate java models for their solution. 

Projects with potential interoperability cases from the eSSIF-Labs Business call 2 group:
* [NYM Srl](https://gitlab.grnet.gr/essif-lab/infrastructure/nym-srl/vca_project_summary) - They are including verification capabilities in their components, these are possibly compatible DIF's PE spec. If so, we should be able to provide them with an example or components for their verification.
* [Jolocom](https://gitlab.grnet.gr/essif-lab/infrastructure/jolocom/cbas_project_summary) - Proving interoperability with this specific project of Jolocom is not really possible, given it entails a different domain. We do want to explore options with Jolocom however given they also have other components that are using W3C/DIF spec based implementations, which could benefit from our work. 
* [Evernym UK Ltd](https://gitlab.grnet.gr/essif-lab/infrastructure/evernym/openup_project_summary) - This project is not a direct match for interoperability because of the use of present-proof/indy, but their mobile SDK could be integrated with the created PE for interoperability testing. 
* [SICPA SPAIN S.L.](https://gitlab.grnet.gr/essif-lab/infrastructure/sicpa/bridge_project_summary) - They are working on components with integration into Aries and are doing VC verification, making this project a good option for interoperability testing. 


### Beyond eSSIF-Labs

One of the eventual goals of our project is to bridge the gap between the W3C-CCG specifications (such as the VC-HTTP-API) and the Hyperledger Aries specifications/implementations. For this purpose, a new work item has been created within the DIF Claims and Credentials working group. This will involve collaboration with representatives in a broad range of SSI spaces (DIF/W3C-CCG/Aries) who seek to define a new test suite and extend/adapt existing specifications and protocols in W3C and Aries to enable compatibility and standardization around verifier/holder interactions.

Sphereon's participation in the group enables us to broaden the target audience of eSSIF-Labs interoperability efforts, and provide a channel for communication and alignment between internal eSSIF-Labs members and the broader SSI community.

