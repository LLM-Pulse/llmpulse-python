# PromptDeleteResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**deleted** | **bool** | Always true | 
**id** | **int** |  | 
**raw_input** | **str** |  | 
**total_after** | **int** | Prompts left in the project | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.prompt_delete_response import PromptDeleteResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PromptDeleteResponse from a JSON string
prompt_delete_response_instance = PromptDeleteResponse.from_json(json)
# print the JSON string representation of the object
print(PromptDeleteResponse.to_json())

# convert the object into a dict
prompt_delete_response_dict = prompt_delete_response_instance.to_dict()
# create an instance of PromptDeleteResponse from a dict
prompt_delete_response_from_dict = PromptDeleteResponse.from_dict(prompt_delete_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


