# RecommendationLaunchResponseRecommendation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Poll GET /recommendations/{id} with it | 
**recommendation_type** | **str** |  | 
**status** | **str** | Always pending | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.recommendation_launch_response_recommendation import RecommendationLaunchResponseRecommendation

# TODO update the JSON string below
json = "{}"
# create an instance of RecommendationLaunchResponseRecommendation from a JSON string
recommendation_launch_response_recommendation_instance = RecommendationLaunchResponseRecommendation.from_json(json)
# print the JSON string representation of the object
print(RecommendationLaunchResponseRecommendation.to_json())

# convert the object into a dict
recommendation_launch_response_recommendation_dict = recommendation_launch_response_recommendation_instance.to_dict()
# create an instance of RecommendationLaunchResponseRecommendation from a dict
recommendation_launch_response_recommendation_from_dict = RecommendationLaunchResponseRecommendation.from_dict(recommendation_launch_response_recommendation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


