# CustomReportFilters


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**models** | **List[str]** | AI models the report covers; empty means every enabled model | 
**collection_ids** | **List[int]** | Tags the report is limited to; empty means every prompt | 
**brand_kind** | **str** |  | [optional] 
**competitor_ids** | **List[int]** | Competitors compared, the report&#39;s own choice or else the Overview selection | 

## Example

```python
from llmpulse.models.custom_report_filters import CustomReportFilters

# TODO update the JSON string below
json = "{}"
# create an instance of CustomReportFilters from a JSON string
custom_report_filters_instance = CustomReportFilters.from_json(json)
# print the JSON string representation of the object
print(CustomReportFilters.to_json())

# convert the object into a dict
custom_report_filters_dict = custom_report_filters_instance.to_dict()
# create an instance of CustomReportFilters from a dict
custom_report_filters_from_dict = CustomReportFilters.from_dict(custom_report_filters_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


