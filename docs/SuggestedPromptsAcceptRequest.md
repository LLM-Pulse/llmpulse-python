# SuggestedPromptsAcceptRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**ids** | **List[int]** | Suggestion ids to accept (max 100) | 
**tag_ids** | **List[int]** | One tag id to put the new prompts in | [optional] 
**tag_names** | **List[str]** | One tag name (case-insensitive) to put the new prompts in | [optional] 
**create_missing** | **bool** | Create the tag named in tag_names when it does not exist | [optional] [default to False]

## Example

```python
from llmpulse.models.suggested_prompts_accept_request import SuggestedPromptsAcceptRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SuggestedPromptsAcceptRequest from a JSON string
suggested_prompts_accept_request_instance = SuggestedPromptsAcceptRequest.from_json(json)
# print the JSON string representation of the object
print(SuggestedPromptsAcceptRequest.to_json())

# convert the object into a dict
suggested_prompts_accept_request_dict = suggested_prompts_accept_request_instance.to_dict()
# create an instance of SuggestedPromptsAcceptRequest from a dict
suggested_prompts_accept_request_from_dict = SuggestedPromptsAcceptRequest.from_dict(suggested_prompts_accept_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


