<h1 align="center">
  <br>
  <a href="https://www.sphereon.com"><img src="https://sphereon.com/content/themes/sphereon/assets/img/logo.svg" alt="Sphereon" width="400"></a>
  <br> Presentation Exchange Credential Query Infra 
  <br> Project Summary
  <br>
</h1>


Sphereon, as part of its Vindicatio project, is creating a new DIF Presentation Exchange (PE) for DIF/W3C SSI solutions. The PE will be compatible with Aries Present Proof Protocol v2, and uses a layered approach to achieve both integration and interoperability.

At the lowest layers there are TypeScript (Javascript) libraries for the rules engine component, validations and logic [Presentation Exchange Library](./interface_specification_of_pe_library_component.md). These libraries are easy to integrate in other projects for both web and mobile. The models and generator will be provided as part of the [PE OpenAPI specification and models generator](./interface_specification_of_pe_openapi_spec_and_models_generator_component.md), allowing the models to be generated to a programming language of choice. Then there is the [Presentation Exchange REST API](./interface_specification_of_pe_rest_api_component.md) which exposes the functionality of the PE to be used in any programming language. The REST Api (and state machine) can run in Docker for a more direct integration. 

For the exchange of credentials there is a stateful bridge that integrates DIDComm v2 and CHAPI (and future OpenID-Connect). The bridge will be similar to Aries Present Proof v2 and integrate with it. In the future support for a backend like Verity or similar can be added. This means parties can talk using Presentation Exchange compatible datastructures, across different transports and with different products.
