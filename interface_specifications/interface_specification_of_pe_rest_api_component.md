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
* [Connection Invitation POST](pe_openapi/apis/v1/a0_pe_invitation_post.md)
* [Connection Invitation GET](pe_openapi/apis/v1/a1_pe_invitation_get.md)
* [Connection POST](pe_openapi/apis/v1/a2_pe_connection_post.md)
* [Presentation Thread POST](pe_openapi/apis/v1/b0_pe_thread_post.md)
* [Presentation Definition POST](pe_openapi/apis/v1/c0_pe_definition_post.md)
* [Presentation Definition GET](pe_openapi/apis/v1/c1_pe_definition_get.md)
* [Presentation POST](pe_openapi/apis/v1/d0_pe_presentation_post.md)
* [Presentation Definition Status PUT](pe_openapi/apis/v1/d1_pe_definition_status_put.md)
* [Presentation GET](pe_openapi/apis/v1/d2_pe_presentation_get.md)
* [Presentations GET](pe_openapi/apis/v1/d3_pe_presentations_get.md)
* [Presentation status POST](pe_openapi/apis/v1/e0_pe_presentation_status_post.md)
* [Presentation status PUT](pe_openapi/apis/v1/e1_pe_presentation_status_put.md)
* [Presentation status GET](pe_openapi/apis/v1/e2_pe_presentation_status_get.md)

