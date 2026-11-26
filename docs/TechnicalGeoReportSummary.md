# TechnicalGeoReportSummary

One technical GEO report's status and score

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**report_type** | **str** | The report_type requested (agent_readiness for ai_readiness) | 
**project_id** | **int** |  | 
**batch_id** | **int** | Bundle the report was created in; null for a report created on its own | 
**url** | **str** | The page analysed; null for the domain-level types (robots_txt, agent_readiness, llms_txt, ai_visibility) | 
**domain** | **str** |  | 
**country_code** | **str** | Set only on llms_txt and ai_visibility reports | 
**output_language_code** | **str** | ISO 639-1 code an llms_txt report was requested in; null for an llms_txt report written in the website&#39;s own language and for every other type | 
**status** | **str** | Depends on report_type. Every type ends completed or failed; ai_visibility can also end insufficient_data | 
**result_available** | **bool** | Whether status is completed | 
**overall_score** | **float** | Null until the report completes, and always for llms_txt | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**app_url** | **str** | Opens this report in the app | [optional] 

## Example

```python
from llmpulse.models.technical_geo_report_summary import TechnicalGeoReportSummary

# TODO update the JSON string below
json = "{}"
# create an instance of TechnicalGeoReportSummary from a JSON string
technical_geo_report_summary_instance = TechnicalGeoReportSummary.from_json(json)
# print the JSON string representation of the object
print(TechnicalGeoReportSummary.to_json())

# convert the object into a dict
technical_geo_report_summary_dict = technical_geo_report_summary_instance.to_dict()
# create an instance of TechnicalGeoReportSummary from a dict
technical_geo_report_summary_from_dict = TechnicalGeoReportSummary.from_dict(technical_geo_report_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


