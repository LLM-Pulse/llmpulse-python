# PromptCategorizationResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**prompt** | [**PromptCategorization**](PromptCategorization.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.prompt_categorization_response import PromptCategorizationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PromptCategorizationResponse from a JSON string
prompt_categorization_response_instance = PromptCategorizationResponse.from_json(json)
# print the JSON string representation of the object
print(PromptCategorizationResponse.to_json())

# convert the object into a dict
prompt_categorization_response_dict = prompt_categorization_response_instance.to_dict()
# create an instance of PromptCategorizationResponse from a dict
prompt_categorization_response_from_dict = PromptCategorizationResponse.from_dict(prompt_categorization_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


