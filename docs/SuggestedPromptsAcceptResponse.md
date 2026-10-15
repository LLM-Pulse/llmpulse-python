# SuggestedPromptsAcceptResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**accepted** | [**List[SuggestedPromptsAcceptResponseAcceptedInner]**](SuggestedPromptsAcceptResponseAcceptedInner.md) |  | 
**skipped** | [**List[CatalogPromptSuggestionsAcceptResponseSkippedInner]**](CatalogPromptSuggestionsAcceptResponseSkippedInner.md) |  | 
**prompts_available** | **int** | Prompt slots left on the plan; null when unlimited | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.suggested_prompts_accept_response import SuggestedPromptsAcceptResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SuggestedPromptsAcceptResponse from a JSON string
suggested_prompts_accept_response_instance = SuggestedPromptsAcceptResponse.from_json(json)
# print the JSON string representation of the object
print(SuggestedPromptsAcceptResponse.to_json())

# convert the object into a dict
suggested_prompts_accept_response_dict = suggested_prompts_accept_response_instance.to_dict()
# create an instance of SuggestedPromptsAcceptResponse from a dict
suggested_prompts_accept_response_from_dict = SuggestedPromptsAcceptResponse.from_dict(suggested_prompts_accept_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


