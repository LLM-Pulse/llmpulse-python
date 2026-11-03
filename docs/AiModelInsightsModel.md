# AiModelInsightsModel


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model** | **str** | AI model key, as /dimensions/models lists it | [optional] 
**label** | **str** | Display name of the model | [optional] 
**color** | **str** | Hex color the app charts the model with | [optional] 

## Example

```python
from llmpulse.models.ai_model_insights_model import AiModelInsightsModel

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelInsightsModel from a JSON string
ai_model_insights_model_instance = AiModelInsightsModel.from_json(json)
# print the JSON string representation of the object
print(AiModelInsightsModel.to_json())

# convert the object into a dict
ai_model_insights_model_dict = ai_model_insights_model_instance.to_dict()
# create an instance of AiModelInsightsModel from a dict
ai_model_insights_model_from_dict = AiModelInsightsModel.from_dict(ai_model_insights_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


