# RecommendationItemUpdateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**item** | [**RecommendationItem**](RecommendationItem.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.recommendation_item_update_response import RecommendationItemUpdateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RecommendationItemUpdateResponse from a JSON string
recommendation_item_update_response_instance = RecommendationItemUpdateResponse.from_json(json)
# print the JSON string representation of the object
print(RecommendationItemUpdateResponse.to_json())

# convert the object into a dict
recommendation_item_update_response_dict = recommendation_item_update_response_instance.to_dict()
# create an instance of RecommendationItemUpdateResponse from a dict
recommendation_item_update_response_from_dict = RecommendationItemUpdateResponse.from_dict(recommendation_item_update_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


