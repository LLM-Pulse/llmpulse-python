# AiModelWeightedVisibilityRow


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model** | **str** | AI model key, as /dimensions/models lists it | [optional] 
**label** | **str** | Display name of the model | [optional] 
**color** | **str** | Hex color the app charts the model with | [optional] 
**weighted_visibility_score** | **float** | The brand&#39;s AI Visibility Score in the model, its points there divided by the days the model answered; 0 when it has none | [optional] 
**share_of_total** | **float** | The model&#39;s percentage (0-100) of the brand&#39;s AI Visibility Score points; null when the brand has none | [optional] 

## Example

```python
from llmpulse.models.ai_model_weighted_visibility_row import AiModelWeightedVisibilityRow

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelWeightedVisibilityRow from a JSON string
ai_model_weighted_visibility_row_instance = AiModelWeightedVisibilityRow.from_json(json)
# print the JSON string representation of the object
print(AiModelWeightedVisibilityRow.to_json())

# convert the object into a dict
ai_model_weighted_visibility_row_dict = ai_model_weighted_visibility_row_instance.to_dict()
# create an instance of AiModelWeightedVisibilityRow from a dict
ai_model_weighted_visibility_row_from_dict = AiModelWeightedVisibilityRow.from_dict(ai_model_weighted_visibility_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


