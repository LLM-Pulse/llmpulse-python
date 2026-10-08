# RecommendationSummarySummary

Empty until the generation completes

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_recommendations** | **int** |  | [optional] 
**high_priority_count** | **int** |  | [optional] 
**categories** | **List[str]** |  | [optional] 

## Example

```python
from llmpulse.models.recommendation_summary_summary import RecommendationSummarySummary

# TODO update the JSON string below
json = "{}"
# create an instance of RecommendationSummarySummary from a JSON string
recommendation_summary_summary_instance = RecommendationSummarySummary.from_json(json)
# print the JSON string representation of the object
print(RecommendationSummarySummary.to_json())

# convert the object into a dict
recommendation_summary_summary_dict = recommendation_summary_summary_instance.to_dict()
# create an instance of RecommendationSummarySummary from a dict
recommendation_summary_summary_from_dict = RecommendationSummarySummary.from_dict(recommendation_summary_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


