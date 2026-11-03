# PromptsCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**created** | **int** |  | [optional] 
**skipped** | **int** |  | [optional] 
**total_after** | **int** |  | [optional] 
**prompts_available** | **int** |  | [optional] 
**tracked** | **bool** | Whether scheduled runs include the project the prompts were added to. False when it is paused or beyond the plan&#39;s project limit, so the new prompts do not run until that changes | [optional] 
**untracked_reason** | **str** | Why tracked is false: pitch_project, paused or project_limit. Null when tracked | [optional] 
**warning** | **str** | What to do when tracked is false, or why some first runs wait when first_runs_wait_until is set. Null otherwise | [optional] 
**first_runs_wait_until** | **datetime** | Set when the account&#39;s allowance of AI answers left this cycle cannot give every new prompt one answer per enabled AI model, so the rest run when the allowance resets at this time (00:00 Europe/Madrid). It counts this request&#39;s prompts against what was left when it arrived, not first runs other requests queued moments earlier. Null otherwise, when the allowance is unlimited, when tracked is false or when the account is not active | [optional] 
**data** | [**List[PromptsCreateResponseDataInner]**](PromptsCreateResponseDataInner.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.prompts_create_response import PromptsCreateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PromptsCreateResponse from a JSON string
prompts_create_response_instance = PromptsCreateResponse.from_json(json)
# print the JSON string representation of the object
print(PromptsCreateResponse.to_json())

# convert the object into a dict
prompts_create_response_dict = prompts_create_response_instance.to_dict()
# create an instance of PromptsCreateResponse from a dict
prompts_create_response_from_dict = PromptsCreateResponse.from_dict(prompts_create_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


