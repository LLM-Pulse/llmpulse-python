# RecommendationSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**project_id** | **int** |  | 
**recommendation_type** | **str** |  | 
**status** | **str** |  | 
**error_message** | **str** | Set only when status is failed | 
**generated_at** | **datetime** | Null until the generation completes | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**total_recommendations** | **int** |  | 
**high_priority_count** | **int** |  | 
**summary** | [**RecommendationSummarySummary**](RecommendationSummarySummary.md) |  | 
**context** | **object** | Generation context and run diagnostics as stored; empty until the generation completes. Its keys are not a stable contract | 

## Example

```python
from llmpulse.models.recommendation_summary import RecommendationSummary

# TODO update the JSON string below
json = "{}"
# create an instance of RecommendationSummary from a JSON string
recommendation_summary_instance = RecommendationSummary.from_json(json)
# print the JSON string representation of the object
print(RecommendationSummary.to_json())

# convert the object into a dict
recommendation_summary_dict = recommendation_summary_instance.to_dict()
# create an instance of RecommendationSummary from a dict
recommendation_summary_from_dict = RecommendationSummary.from_dict(recommendation_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


