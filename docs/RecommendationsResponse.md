# RecommendationsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[RecommendationSummary]**](RecommendationSummary.md) |  | 

## Example

```python
from llmpulse.models.recommendations_response import RecommendationsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RecommendationsResponse from a JSON string
recommendations_response_instance = RecommendationsResponse.from_json(json)
# print the JSON string representation of the object
print(RecommendationsResponse.to_json())

# convert the object into a dict
recommendations_response_dict = recommendations_response_instance.to_dict()
# create an instance of RecommendationsResponse from a dict
recommendations_response_from_dict = RecommendationsResponse.from_dict(recommendations_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


