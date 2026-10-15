# RecommendationItem

One recommendation item, in the shape GET /recommendations/{id} lists items

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**recommendation_id** | **int** |  | 
**recommendation_type** | **str** |  | 
**category** | **str** |  | 
**title** | **str** |  | 
**description** | **str** |  | [optional] 
**priority** | **str** |  | 
**estimated_impact** | **str** |  | [optional] 
**action_items** | **List[str]** |  | 
**source_refs** | **List[str]** | Evidence codes (e.g. P1, C2) resolved in resolved_source_refs | 
**status** | **str** |  | 
**status_changed_at** | **datetime** |  | [optional] 
**position** | **int** |  | 
**metadata** | **Dict[str, object]** |  | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**resolved_source_refs** | **List[Dict[str, object]]** | The evidence each source_refs code points to (prompt, citation or own page) | [optional] 
**unresolved_source_refs** | **List[str]** | Present only when a code points to no stored evidence | [optional] 

## Example

```python
from llmpulse.models.recommendation_item import RecommendationItem

# TODO update the JSON string below
json = "{}"
# create an instance of RecommendationItem from a JSON string
recommendation_item_instance = RecommendationItem.from_json(json)
# print the JSON string representation of the object
print(RecommendationItem.to_json())

# convert the object into a dict
recommendation_item_dict = recommendation_item_instance.to_dict()
# create an instance of RecommendationItem from a dict
recommendation_item_from_dict = RecommendationItem.from_dict(recommendation_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


