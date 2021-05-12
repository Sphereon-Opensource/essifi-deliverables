# Functional Specification of PE REST API

Sphereon's PE REST API is the easiest, implementation agnostic, stateful & platform independent way to leverage the power of [DIF Presentation Exchange v1.0.0 specification](https://identity.foundation/presentation-exchange/) without needing to implement any of the DIF PE logic. While PE REST API takes no assumptions about holder's implementation, a holder can benefit greatly by using PE Library as a dependency in the system to submit the response with high certainty of acceptance.

The PE REST API exposes simple APIs to be called from any client side or server side system and provides easy to use callbacks to be notified about the status of presentation exchange. PE REST API is asynchronous and provides alternative mechanisms to both verifier and holders of verifiable credentials to progress the exchange of the credentials.

Systems which need a stateful, reliable and compliant DIF exchange can use PE REST API with a simple create session call, enabling the caller to have a sharable presentation definition. On each progressive interaction with the PE REST API backend updates and keeps track of the status of exchange. This status can be notified to the parties over the provided endpoint. The parties can also enquire the status by calling status check API eliminating the need to develop and deploy a callback listening endpoint.

PE REST API being agnostic to callers' implementation allows the verifier and holders to be interchangeable. A holder can potentially initiate a verification for some entity that they want to connect to.