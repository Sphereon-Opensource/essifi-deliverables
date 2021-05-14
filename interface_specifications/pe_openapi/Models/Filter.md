# Filter
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | [**String**](string.md) | Object type of the acceptable field. | [default to null]
**format** | [**String**](string.md) | format in which the item is expected. e.g. date time format of some sort. | [optional] [default to null]
**pattern** | [**String**](string.md) | The regular expression that can help filter the target object. | [optional] [default to null]
**minLength** | [**Integer**](integer.md) | acceptable minimum length (e.g. of string) that is acceptable | [optional] [default to null]
**maxLength** | [**Integer**](integer.md) | acceptable maximum length (e.g. of string) that is acceptable | [optional] [default to null]
**minimum** | [**BigDecimal**](number.md) | acceptable minimum value (e.g. 0) that is acceptable for the number including this number (i.e. 0 in this case) | [optional] [default to null]
**exclusiveMinimum** | [**BigDecimal**](number.md) | acceptable minimum value (e.g. 0) that is acceptable for the number exclusive of the number (i.e. 0 in this case) | [optional] [default to null]
**exclusiveMaximum** | [**BigDecimal**](number.md) | acceptable maximum value (e.g. 100) that is acceptable for the number exclusive of the number (i.e. 100 in this case) | [optional] [default to null]
**maximum** | [**BigDecimal**](number.md) | acceptable maximum value (e.g. 100) that is acceptable for the number including this number (i.e. 100 in this case) | [optional] [default to null]
**const** | [**BigDecimal**](number.md) | A fixed value that is accpetable in this variable | [optional] [default to null]
**enum** | [**List**](number.md) |  | [optional] [default to null]
**not** | [**Object**](.md) | The values which will make the item unacceptable | [optional] [default to null]

[[Back to Model list]](../interface_specification_of_pe_openapi_spec_component.md#documentation-for-models) [[Back to API list]](../interface_specification_of_pe_openapi_spec_component.md#documentation-for-api-endpoints) [[Back to README]](../interface_specification_of_pe_openapi_spec_component.md)

