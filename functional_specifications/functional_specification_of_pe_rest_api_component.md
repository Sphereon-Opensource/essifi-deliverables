# Functional Specification of PE REST API

Sphereon's PE REST API is an implementation agnostic, stateful, and platform independent way to leverage the power of [DIF Presentation Exchange v1.0.0 specification](https://identity.foundation/presentation-exchange/). The API can be used without having to implement any of the DIF PE logic yourself. While the PE REST API takes no assumptions about holder's implementation, a holder can benefit greatly by using the PE Library as a dependency in the system, as it allows them to submit the presentation(s) with a certainty of acceptance. The PE Library will ensure that the information submitted in the response is compatible with the request model of the verifier.

Systems that need a stateful, reliable and compliant DIF Presentation Exchange can use PE REST API with a simple 'create session' call. This will enable the caller to have a presentation definition that can be shared. On each progressive interaction with the PE REST API, the backend will be updated, keeping track of the status of the overall exchange. The involved parties can be notified of the status changes using the provided endpoint. The parties can also enquire the status by calling the 'status check' API endpoint, eliminating the need to develop and deploy a callback listening endpoint. The fact that the PE REST API is agnostic to the callers' implementation, allows the verifier and holders to be interchangeable and have different systems.

The rest API supports the following actions:
    - create presentation definition
    - submit presentation
    - check/update status

For more details on the specific actions that are available, see the [Sphereon's Presentation Exchange REST API Interface specification](./interface_specification/interface_specification_of_pe_rest_api_component.md)
