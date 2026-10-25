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
**untracked_reason** | **str** | Why tracked is false: paused or project_limit. Null when tracked | [optional] 
**warning** | **str** | What to do when tracked is false. Null when tracked | [optional] 
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


