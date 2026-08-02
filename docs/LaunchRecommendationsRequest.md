# LaunchRecommendationsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**recommendation_type** | **str** |  | [optional] [default to 'ai_visibility']

## Example

```python
from llmpulse.models.launch_recommendations_request import LaunchRecommendationsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of LaunchRecommendationsRequest from a JSON string
launch_recommendations_request_instance = LaunchRecommendationsRequest.from_json(json)
# print the JSON string representation of the object
print(LaunchRecommendationsRequest.to_json())

# convert the object into a dict
launch_recommendations_request_dict = launch_recommendations_request_instance.to_dict()
# create an instance of LaunchRecommendationsRequest from a dict
launch_recommendations_request_from_dict = LaunchRecommendationsRequest.from_dict(launch_recommendations_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


