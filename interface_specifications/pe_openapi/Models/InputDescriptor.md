# InputDescriptor
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | [**String**](string.md) | The verifiable credentials that is acceptable from the holder. e.g. wa_driver_license | [default to null]
**name** | [**String**](string.md) | The verifiable credentials that is acceptable from the holder in a human readibly string form. i.e. an alternative for the humans to the id | [optional] [default to null]
**purpose** | [**String**](string.md) | It describes the purpose for which the Presentation Definition&#39;s inputs are being requested. | [optional] [default to null]
**group** | [**List**](string.md) | A group from which the specific credential is required. | [optional] [default to null]
**schema** | [**List**](Schema.md) |  | [default to null]
**constraints** | [**Constraints**](Constraints.md) |  | [optional] [default to null]

[[Back to Model list]](../interface_specification_of_pe_openapi_spec_component.md#documentation-for-models) [[Back to API list]](../interface_specification_of_pe_openapi_spec_component.md#documentation-for-api-endpoints) [[Back to README]](../interface_specification_of_pe_openapi_spec_component.md)

