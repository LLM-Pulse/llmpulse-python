# TechnicalGeoReportsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**report_type** | **str** | The report_type requested (agent_readiness for ai_readiness) | 
**data** | [**List[TechnicalGeoReportSummary]**](TechnicalGeoReportSummary.md) |  | 

## Example

```python
from llmpulse.models.technical_geo_reports_response import TechnicalGeoReportsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TechnicalGeoReportsResponse from a JSON string
technical_geo_reports_response_instance = TechnicalGeoReportsResponse.from_json(json)
# print the JSON string representation of the object
print(TechnicalGeoReportsResponse.to_json())

# convert the object into a dict
technical_geo_reports_response_dict = technical_geo_reports_response_instance.to_dict()
# create an instance of TechnicalGeoReportsResponse from a dict
technical_geo_reports_response_from_dict = TechnicalGeoReportsResponse.from_dict(technical_geo_reports_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


