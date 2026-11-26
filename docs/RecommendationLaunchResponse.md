# RecommendationLaunchResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**recommendation** | [**RecommendationLaunchResponseRecommendation**](RecommendationLaunchResponseRecommendation.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.recommendation_launch_response import RecommendationLaunchResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RecommendationLaunchResponse from a JSON string
recommendation_launch_response_instance = RecommendationLaunchResponse.from_json(json)
# print the JSON string representation of the object
print(RecommendationLaunchResponse.to_json())

# convert the object into a dict
recommendation_launch_response_dict = recommendation_launch_response_instance.to_dict()
# create an instance of RecommendationLaunchResponse from a dict
recommendation_launch_response_from_dict = RecommendationLaunchResponse.from_dict(recommendation_launch_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


