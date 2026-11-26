# RecommendationDetailResponseSummary

Empty until the generation completes

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_recommendations** | **int** |  | [optional] 
**high_priority_count** | **int** |  | [optional] 
**categories** | **List[str]** |  | [optional] 

## Example

```python
from llmpulse.models.recommendation_detail_response_summary import RecommendationDetailResponseSummary

# TODO update the JSON string below
json = "{}"
# create an instance of RecommendationDetailResponseSummary from a JSON string
recommendation_detail_response_summary_instance = RecommendationDetailResponseSummary.from_json(json)
# print the JSON string representation of the object
print(RecommendationDetailResponseSummary.to_json())

# convert the object into a dict
recommendation_detail_response_summary_dict = recommendation_detail_response_summary_instance.to_dict()
# create an instance of RecommendationDetailResponseSummary from a dict
recommendation_detail_response_summary_from_dict = RecommendationDetailResponseSummary.from_dict(recommendation_detail_response_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


