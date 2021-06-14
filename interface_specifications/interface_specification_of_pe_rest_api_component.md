# Interface Specification for Presentation Exchange REST API

The goal of the REST API for Presentation Exchange is to:

* Expose the functionality of the [PE Library](./interface_specification_of_pe_library_component.md) for use in any language
* Provide stateful interaction mediation between holders and verifiers


## Legends

<br/>

![image info](./figures/Legends.svg)


## PE REST API Connection Flow
<br/>

![image info](./figures/PE_REST_API_connection_sequence.svg)

## PE REST API Presentation Exchange

<br/>

![image info](./figures/PE_REST_API_sequence.svg)


## API
* [Connection Invitation POST](pe_openapi/apis/v1/pe_invitation_post.md)
* [Connection Invitation GET](pe_openapi/apis/v1/pe_invitation_get.md)
* [Presentation Definition POST](./pe_openapi/apis/v1/pe_definition_post.md)
* [Presentation Definition Challenge GET](./pe_openapi/apis/v1/pe_definition_get.md)
* [Presentation POST](./pe_openapi/apis/v1/pe_presentation_post.md)
* [Status Notification to Party](./pe_openapi/apis/v1/pe_presentation_status_push.md)
* [Verifiable Presentation GET](./pe_openapi/apis/v1/pe_presentation_get.md)
* [Status POST](pe_openapi/apis/v1/pe_presentation_status_post.md)
* [Status GET](./pe_openapi/apis/v1/pe_definition_get.md)

