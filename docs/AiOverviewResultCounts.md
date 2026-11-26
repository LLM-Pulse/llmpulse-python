# AiOverviewResultCounts


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_responses** | **int** | AI Overview runs in the window | 
**responses_with_results** | **int** | Runs that returned an AI Overview | 
**result_rate** | **float** |  | 

## Example

```python
from llmpulse.models.ai_overview_result_counts import AiOverviewResultCounts

# TODO update the JSON string below
json = "{}"
# create an instance of AiOverviewResultCounts from a JSON string
ai_overview_result_counts_instance = AiOverviewResultCounts.from_json(json)
# print the JSON string representation of the object
print(AiOverviewResultCounts.to_json())

# convert the object into a dict
ai_overview_result_counts_dict = ai_overview_result_counts_instance.to_dict()
# create an instance of AiOverviewResultCounts from a dict
ai_overview_result_counts_from_dict = AiOverviewResultCounts.from_dict(ai_overview_result_counts_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


