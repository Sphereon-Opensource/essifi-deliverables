# SubmissionRequirement1
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | [**String**](string.md) | what verifiable credential is demanded in order for the presentation to be sensible. | [optional] [default to null]
**purpose** | [**String**](string.md) | Why this verifiable credentials is requested. | [optional] [default to null]
**rule** | [**String**](string.md) | Whether all the requirements are mandatory or holder has multiple options to select verifiable credentials from | [default to null]
**count** | [**Integer**](integer.md) | How many of the credentials are demanded for the presentation to be sensible. | [optional] [default to null]
**min** | [**Integer**](integer.md) | Minimum of the credentials are demanded for the presentation to be sensible. | [optional] [default to null]
**max** | [**Integer**](integer.md) | Maximum of the credentials are demanded for the presentation to be sensible. | [optional] [default to null]
**from** | [**String**](string.md) | One of the group strings specified for one or more [[ref:Input Descriptor Objects]. | [optional] [default to null]
**from\_nested** | [**List**](Submission_Requirement.md) | nested submission_requirement and is a way to organize the requirements. For example requirements mentioned in the flat list will also be able to provide same information but will be less organized. | [optional] [default to null]

[[Back to Model list]](../interface_specification_of_pe_openapi_spec_component.md#documentation-for-models) [[Back to API list]](../interface_specification_of_pe_openapi_spec_component.md#documentation-for-api-endpoints) [[Back to README]](../interface_specification_of_pe_openapi_spec_component.md)

