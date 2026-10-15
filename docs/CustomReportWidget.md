# CustomReportWidget


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | 
**label** | **str** |  | 
**kind** | **str** |  | 
**width** | **str** |  | 
**available** | **bool** | false when the widget&#39;s data source (web analytics, agent analytics, owned media) is not connected | 
**data** | **Dict[str, object]** | Shaped by kind. timeseries: series [{ name, color, points [{ date, value }] }]. donut: slices [{ name, value, color }]. bar: bars [{ label, value, color }]. kpi_grid: values and changes (null unless the report compares with the previous period). table: rows, one object per row. Null when the widget is not available. | [optional] 

## Example

```python
from llmpulse.models.custom_report_widget import CustomReportWidget

# TODO update the JSON string below
json = "{}"
# create an instance of CustomReportWidget from a JSON string
custom_report_widget_instance = CustomReportWidget.from_json(json)
# print the JSON string representation of the object
print(CustomReportWidget.to_json())

# convert the object into a dict
custom_report_widget_dict = custom_report_widget_instance.to_dict()
# create an instance of CustomReportWidget from a dict
custom_report_widget_from_dict = CustomReportWidget.from_dict(custom_report_widget_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


