# AiModelInsightsReportFiltersEcho

The filters a position distribution or AI Overview report was computed with, as the server resolved them. A filter that was not given is left out, except from, to, granularity and competitors.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_from** | **datetime** |  | 
**to** | **datetime** |  | 
**granularity** | **str** |  | 
**country_code** | **str** | Comma-separated country codes | [optional] 
**language_code** | **str** | Comma-separated language codes | [optional] 
**collection_id** | **str** | Comma-separated collection ids | [optional] 
**prompt_type** | **str** | Comma-separated prompt types | [optional] 
**brand_kind** | **str** |  | [optional] 
**model** | **str** | The model filter; always ai_overview on the AI Overview report | [optional] 
**competitors** | **List[int]** | Competitor ids from the competitors parameter; empty when it was not given | 
**brand1** | **str** | Position distribution only. The id, as a string, of the competitor compared as the first brand; left out for the project brand | [optional] 
**brand2** | **str** | Position distribution only. The id, as a string, of the competitor compared as the second brand, by default the competitor with the most mentions; left out when the project has none to compare | [optional] 

## Example

```python
from llmpulse.models.ai_model_insights_report_filters_echo import AiModelInsightsReportFiltersEcho

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelInsightsReportFiltersEcho from a JSON string
ai_model_insights_report_filters_echo_instance = AiModelInsightsReportFiltersEcho.from_json(json)
# print the JSON string representation of the object
print(AiModelInsightsReportFiltersEcho.to_json())

# convert the object into a dict
ai_model_insights_report_filters_echo_dict = ai_model_insights_report_filters_echo_instance.to_dict()
# create an instance of AiModelInsightsReportFiltersEcho from a dict
ai_model_insights_report_filters_echo_from_dict = AiModelInsightsReportFiltersEcho.from_dict(ai_model_insights_report_filters_echo_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


