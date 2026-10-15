# SuggestedPromptIdsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**ids** | **List[int]** | Suggestion ids (max 100) | 

## Example

```python
from llmpulse.models.suggested_prompt_ids_request import SuggestedPromptIdsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SuggestedPromptIdsRequest from a JSON string
suggested_prompt_ids_request_instance = SuggestedPromptIdsRequest.from_json(json)
# print the JSON string representation of the object
print(SuggestedPromptIdsRequest.to_json())

# convert the object into a dict
suggested_prompt_ids_request_dict = suggested_prompt_ids_request_instance.to_dict()
# create an instance of SuggestedPromptIdsRequest from a dict
suggested_prompt_ids_request_from_dict = SuggestedPromptIdsRequest.from_dict(suggested_prompt_ids_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


