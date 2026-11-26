# AiOverviewResultsResponse

How often Google AI Overviews returned a result for the project's prompts. A result rate is a percentage (0-100) of the AI Overview runs, 0 when there is none.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**var_from** | **datetime** |  | 
**to** | **datetime** |  | 
**filters** | [**AiModelInsightsReportFiltersEcho**](AiModelInsightsReportFiltersEcho.md) |  | 
**granularity** | **str** |  | 
**summary** | [**AiOverviewResultCounts**](AiOverviewResultCounts.md) |  | 
**chart** | [**List[AiOverviewResultsResponseChartInner]**](AiOverviewResultsResponseChartInner.md) | One point per period of the window, oldest first, 0 included | 
**by_prompt** | [**AiOverviewResultsResponseByPrompt**](AiOverviewResultsResponseByPrompt.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.ai_overview_results_response import AiOverviewResultsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AiOverviewResultsResponse from a JSON string
ai_overview_results_response_instance = AiOverviewResultsResponse.from_json(json)
# print the JSON string representation of the object
print(AiOverviewResultsResponse.to_json())

# convert the object into a dict
ai_overview_results_response_dict = ai_overview_results_response_instance.to_dict()
# create an instance of AiOverviewResultsResponse from a dict
ai_overview_results_response_from_dict = AiOverviewResultsResponse.from_dict(ai_overview_results_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


