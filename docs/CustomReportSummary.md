# CustomReportSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 
**date_range** | [**CustomReportDateRange**](CustomReportDateRange.md) |  | 
**schedule** | [**CustomReportSchedule**](CustomReportSchedule.md) |  | 
**recipients_count** | **int** |  | 
**published** | **bool** | Whether the shared link is published | 
**public_link_active** | **bool** | Whether the shared link opens (published and not made inside a client portal) | 
**password_protected** | **bool** |  | 
**portal_only** | **bool** | Made inside a client portal, so it cannot be shared or emailed | 
**widget_count** | **int** |  | 
**widgets** | [**List[CustomReportWidgetRef]**](CustomReportWidgetRef.md) |  | 
**last_sent_at** | **datetime** | When the report was last emailed, on its schedule or with Send now | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.custom_report_summary import CustomReportSummary

# TODO update the JSON string below
json = "{}"
# create an instance of CustomReportSummary from a JSON string
custom_report_summary_instance = CustomReportSummary.from_json(json)
# print the JSON string representation of the object
print(CustomReportSummary.to_json())

# convert the object into a dict
custom_report_summary_dict = custom_report_summary_instance.to_dict()
# create an instance of CustomReportSummary from a dict
custom_report_summary_from_dict = CustomReportSummary.from_dict(custom_report_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


