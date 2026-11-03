# AiModelWeightedVisibilityCell


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **float** | The actor&#39;s AI Visibility Score points in the model; 0 when it has none | [optional] 

## Example

```python
from llmpulse.models.ai_model_weighted_visibility_cell import AiModelWeightedVisibilityCell

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelWeightedVisibilityCell from a JSON string
ai_model_weighted_visibility_cell_instance = AiModelWeightedVisibilityCell.from_json(json)
# print the JSON string representation of the object
print(AiModelWeightedVisibilityCell.to_json())

# convert the object into a dict
ai_model_weighted_visibility_cell_dict = ai_model_weighted_visibility_cell_instance.to_dict()
# create an instance of AiModelWeightedVisibilityCell from a dict
ai_model_weighted_visibility_cell_from_dict = AiModelWeightedVisibilityCell.from_dict(ai_model_weighted_visibility_cell_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


