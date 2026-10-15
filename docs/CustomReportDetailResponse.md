# CustomReportDetailResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**id** | **int** |  | 
**name** | **str** |  | 
**date_range** | [**CustomReportDateRange**](CustomReportDateRange.md) |  | 
**schedule** | [**CustomReportSchedule**](CustomReportSchedule.md) |  | 
**recipients_count** | **int** |  | [optional] 
**published** | **bool** |  | [optional] 
**public_link_active** | **bool** |  | [optional] 
**password_protected** | **bool** |  | [optional] 
**portal_only** | **bool** |  | [optional] 
**last_sent_at** | **datetime** | When the report was last emailed, on its schedule or with Send now | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**filters** | [**CustomReportFilters**](CustomReportFilters.md) |  | 
**compare_previous** | **bool** |  | [optional] 
**attach_excel** | **bool** |  | [optional] 
**manual_send_available_at** | **datetime** | When the 10-minute cooldown after the last manual send ends; null when none is running | [optional] 
**generated_at** | **datetime** |  | 
**blocks** | [**List[CustomReportBlock]**](CustomReportBlock.md) | The report layout in order | 
**widgets** | [**List[CustomReportWidget]**](CustomReportWidget.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.custom_report_detail_response import CustomReportDetailResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CustomReportDetailResponse from a JSON string
custom_report_detail_response_instance = CustomReportDetailResponse.from_json(json)
# print the JSON string representation of the object
print(CustomReportDetailResponse.to_json())

# convert the object into a dict
custom_report_detail_response_dict = custom_report_detail_response_instance.to_dict()
# create an instance of CustomReportDetailResponse from a dict
custom_report_detail_response_from_dict = CustomReportDetailResponse.from_dict(custom_report_detail_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


