# SuggestedPromptsRejectResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**rejected** | **int** |  | 
**ids** | **List[int]** | The suggestions that were pending and are now rejected | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.suggested_prompts_reject_response import SuggestedPromptsRejectResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SuggestedPromptsRejectResponse from a JSON string
suggested_prompts_reject_response_instance = SuggestedPromptsRejectResponse.from_json(json)
# print the JSON string representation of the object
print(SuggestedPromptsRejectResponse.to_json())

# convert the object into a dict
suggested_prompts_reject_response_dict = suggested_prompts_reject_response_instance.to_dict()
# create an instance of SuggestedPromptsRejectResponse from a dict
suggested_prompts_reject_response_from_dict = SuggestedPromptsRejectResponse.from_dict(suggested_prompts_reject_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


