# AiModelWeightedVisibilityMatrixActor

An actor (the standard actor shape) with one AI Visibility Score cell per model

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | [optional] 
**id** | **int** | Project id, or competitor id | [optional] 
**competitor_id** | **int** | Null for the project, the competitor id otherwise | [optional] 
**name** | **str** |  | [optional] 
**domain** | **str** | Bare (scheme-less) domain. Null for the project actor when the project has no URL. | [optional] 
**total_weighted_visibility_score** | **float** | The actor&#39;s AI Visibility Score points summed over the models | [optional] 
**models** | [**Dict[str, AiModelWeightedVisibilityCell]**](AiModelWeightedVisibilityCell.md) | One cell per model, keyed by model | [optional] 

## Example

```python
from llmpulse.models.ai_model_weighted_visibility_matrix_actor import AiModelWeightedVisibilityMatrixActor

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelWeightedVisibilityMatrixActor from a JSON string
ai_model_weighted_visibility_matrix_actor_instance = AiModelWeightedVisibilityMatrixActor.from_json(json)
# print the JSON string representation of the object
print(AiModelWeightedVisibilityMatrixActor.to_json())

# convert the object into a dict
ai_model_weighted_visibility_matrix_actor_dict = ai_model_weighted_visibility_matrix_actor_instance.to_dict()
# create an instance of AiModelWeightedVisibilityMatrixActor from a dict
ai_model_weighted_visibility_matrix_actor_from_dict = AiModelWeightedVisibilityMatrixActor.from_dict(ai_model_weighted_visibility_matrix_actor_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


