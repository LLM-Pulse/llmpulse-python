# CustomReportSchedule


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | 
**day_of_week** | **int** | 0 (Sunday) to 6 (Saturday) | [optional] 
**hour** | **int** |  | [optional] 
**timezone** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.custom_report_schedule import CustomReportSchedule

# TODO update the JSON string below
json = "{}"
# create an instance of CustomReportSchedule from a JSON string
custom_report_schedule_instance = CustomReportSchedule.from_json(json)
# print the JSON string representation of the object
print(CustomReportSchedule.to_json())

# convert the object into a dict
custom_report_schedule_dict = custom_report_schedule_instance.to_dict()
# create an instance of CustomReportSchedule from a dict
custom_report_schedule_from_dict = CustomReportSchedule.from_dict(custom_report_schedule_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


