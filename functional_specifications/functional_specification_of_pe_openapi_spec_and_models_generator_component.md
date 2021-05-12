# Functional Specification of PE OpenAPI Models Library & Generator

The PE OpenAPI Models Library & Generator will enable developers to use [DIF Presentation Exchange v1.0.0 specification](https://identity.foundation/presentation-exchange/) in their SSI systems. A standardised presentation exchange is crucial for interoperability between different systems that are used by [verifiers](https://identity.foundation/presentation-exchange/#terminology) and [holders](https://identity.foundation/presentation-exchange/#terminology) (e.g. wallets).

The PE-OpenAPI will enable verifier- and holder-systems to interpret models used by each other in consistent way. Having the model library and generator available will allow for usecases where one wants to implement their own Presentation Exchange, possibly using different programming languages.


## Table of contents

- [PE-OpenAPI specification](#pe-openapi-specification)
- [PE-OpenAPI Models Generator](#pe-openapi-models-generator)
- [PE-Models library](#pe-models-library)


#### PE-OpenAPI specification

The PE-OpenAPI specification is a set of OpenAPI 3 specification YAML files compatible with the [DIF Presentation Exchange v1.0.0 specification](https://identity.foundation/presentation-exchange/). It can be used by 3rd parties to generate the models and SDKs for their own desired framework and programming language. The specification is used to create the Typescript models as described below. Further, Sphereon will use the DIF PE OpenAPI specification to generate the models and SDKs for Sphereon's PE-Library (PE-JS).


#### PE-OpenAPI Models Generator

The PE-OpenAPI Models Generator is a pre-configured component to generate the models from the above PE-OpenAPI v3 Specification YAML files. Developers who intend to integrate the DIF PE specification in their typescript/javascript systems can extend this project or follow the guide to make it part of their code-bases.


#### PE-Models library

The pe-models library is a pre-published ready to use `typescript` `node-module` that can be directly downloaded and installed from `npmjs.com`. This can be used in any javascript based project to have a consistent structure of the models required in presentation exchange between verifier and holders of verifiable credentials.

The PE-Models library will also be used in the libraries desiring to validate and verify presentation definitions and submissions.
