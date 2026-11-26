# AiOverviewResultsResponseChartInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** | First day of the period | 
**total_responses** | **int** |  | 
**responses_with_results** | **int** |  | 
**result_rate** | **float** |  | 

## Example

```python
from llmpulse.models.ai_overview_results_response_chart_inner import AiOverviewResultsResponseChartInner

# TODO update the JSON string below
json = "{}"
# create an instance of AiOverviewResultsResponseChartInner from a JSON string
ai_overview_results_response_chart_inner_instance = AiOverviewResultsResponseChartInner.from_json(json)
# print the JSON string representation of the object
print(AiOverviewResultsResponseChartInner.to_json())

# convert the object into a dict
ai_overview_results_response_chart_inner_dict = ai_overview_results_response_chart_inner_instance.to_dict()
# create an instance of AiOverviewResultsResponseChartInner from a dict
ai_overview_results_response_chart_inner_from_dict = AiOverviewResultsResponseChartInner.from_dict(ai_overview_results_response_chart_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


