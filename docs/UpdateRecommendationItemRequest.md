# UpdateRecommendationItemRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**status** | **str** | completed, archived, or active to restore the item | 

## Example

```python
from llmpulse.models.update_recommendation_item_request import UpdateRecommendationItemRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateRecommendationItemRequest from a JSON string
update_recommendation_item_request_instance = UpdateRecommendationItemRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateRecommendationItemRequest.to_json())

# convert the object into a dict
update_recommendation_item_request_dict = update_recommendation_item_request_instance.to_dict()
# create an instance of UpdateRecommendationItemRequest from a dict
update_recommendation_item_request_from_dict = UpdateRecommendationItemRequest.from_dict(update_recommendation_item_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


