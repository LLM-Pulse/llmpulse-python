# CustomReportDateRange


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | rolling (the last range_days days), previous_month (the previous calendar month), previous_3_months (the 3 calendar months before the current one) or custom (fixed dates, custom_from to custom_to) | 
**range_days** | **int** | Length of a rolling window; null for the other types | 
**custom_from** | **date** | First day chosen for a custom range; null for the other types | 
**custom_to** | **date** | Last day chosen for a custom range, which can be after today; null for the other types | 
**var_from** | **date** | First day of the window as of now (detail only) | [optional] 
**to** | **date** | Last day of the window as of now (detail only); a custom range stops at today | [optional] 
**label** | **str** | The window as the report shows it (detail only) | [optional] 

## Example

```python
from llmpulse.models.custom_report_date_range import CustomReportDateRange

# TODO update the JSON string below
json = "{}"
# create an instance of CustomReportDateRange from a JSON string
custom_report_date_range_instance = CustomReportDateRange.from_json(json)
# print the JSON string representation of the object
print(CustomReportDateRange.to_json())

# convert the object into a dict
custom_report_date_range_dict = custom_report_date_range_instance.to_dict()
# create an instance of CustomReportDateRange from a dict
custom_report_date_range_from_dict = CustomReportDateRange.from_dict(custom_report_date_range_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


