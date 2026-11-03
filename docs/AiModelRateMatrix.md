# AiModelRateMatrix

Each actor's rate within each model: mentions of the actor (mentions_market_share), or answers citing it (citations_market_share), per answer of the model. Rates are independent, so the actors of a model can add up to more or less than 100.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**denominators_by_model** | **Dict[str, int]** | Answers of each model in the window, keyed by model | [optional] 
**actors** | [**List[AiModelRateMatrixActor]**](AiModelRateMatrixActor.md) | The project and each competitor with a mention (or citation) in the window (only the competitors given in competitors, when it is given), by total descending | [optional] 

## Example

```python
from llmpulse.models.ai_model_rate_matrix import AiModelRateMatrix

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelRateMatrix from a JSON string
ai_model_rate_matrix_instance = AiModelRateMatrix.from_json(json)
# print the JSON string representation of the object
print(AiModelRateMatrix.to_json())

# convert the object into a dict
ai_model_rate_matrix_dict = ai_model_rate_matrix_instance.to_dict()
# create an instance of AiModelRateMatrix from a dict
ai_model_rate_matrix_from_dict = AiModelRateMatrix.from_dict(ai_model_rate_matrix_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


