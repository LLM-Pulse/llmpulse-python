# SuggestedPromptsAcceptResponseAcceptedInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**suggestion_id** | **int** |  | 
**prompt_id** | **int** |  | 
**collection_id** | **int** | The tag the prompt was put in; null when no tag was given | 

## Example

```python
from llmpulse.models.suggested_prompts_accept_response_accepted_inner import SuggestedPromptsAcceptResponseAcceptedInner

# TODO update the JSON string below
json = "{}"
# create an instance of SuggestedPromptsAcceptResponseAcceptedInner from a JSON string
suggested_prompts_accept_response_accepted_inner_instance = SuggestedPromptsAcceptResponseAcceptedInner.from_json(json)
# print the JSON string representation of the object
print(SuggestedPromptsAcceptResponseAcceptedInner.to_json())

# convert the object into a dict
suggested_prompts_accept_response_accepted_inner_dict = suggested_prompts_accept_response_accepted_inner_instance.to_dict()
# create an instance of SuggestedPromptsAcceptResponseAcceptedInner from a dict
suggested_prompts_accept_response_accepted_inner_from_dict = SuggestedPromptsAcceptResponseAcceptedInner.from_dict(suggested_prompts_accept_response_accepted_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


