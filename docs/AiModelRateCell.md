# AiModelRateCell


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **float** | numerator as a percentage (0-100) of denominator; null when the model has no answers in the window | [optional] 
**numerator** | **int** | Mentions of the actor (or answers citing it) in the model&#39;s answers | [optional] 
**denominator** | **int** | Answers of the model in the window | [optional] 

## Example

```python
from llmpulse.models.ai_model_rate_cell import AiModelRateCell

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelRateCell from a JSON string
ai_model_rate_cell_instance = AiModelRateCell.from_json(json)
# print the JSON string representation of the object
print(AiModelRateCell.to_json())

# convert the object into a dict
ai_model_rate_cell_dict = ai_model_rate_cell_instance.to_dict()
# create an instance of AiModelRateCell from a dict
ai_model_rate_cell_from_dict = AiModelRateCell.from_dict(ai_model_rate_cell_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


