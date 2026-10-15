# CustomReportWidgetRef


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | 
**label** | **str** |  | 
**kind** | **str** |  | 

## Example

```python
from llmpulse.models.custom_report_widget_ref import CustomReportWidgetRef

# TODO update the JSON string below
json = "{}"
# create an instance of CustomReportWidgetRef from a JSON string
custom_report_widget_ref_instance = CustomReportWidgetRef.from_json(json)
# print the JSON string representation of the object
print(CustomReportWidgetRef.to_json())

# convert the object into a dict
custom_report_widget_ref_dict = custom_report_widget_ref_instance.to_dict()
# create an instance of CustomReportWidgetRef from a dict
custom_report_widget_ref_from_dict = CustomReportWidgetRef.from_dict(custom_report_widget_ref_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


