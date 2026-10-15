# CustomReportBlock


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**key** | **str** | The widget key, for a widget block | [optional] 
**text** | **str** | The text of a heading or text block | [optional] 

## Example

```python
from llmpulse.models.custom_report_block import CustomReportBlock

# TODO update the JSON string below
json = "{}"
# create an instance of CustomReportBlock from a JSON string
custom_report_block_instance = CustomReportBlock.from_json(json)
# print the JSON string representation of the object
print(CustomReportBlock.to_json())

# convert the object into a dict
custom_report_block_dict = custom_report_block_instance.to_dict()
# create an instance of CustomReportBlock from a dict
custom_report_block_from_dict = CustomReportBlock.from_dict(custom_report_block_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


