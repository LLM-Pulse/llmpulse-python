# PromptsCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**created** | **int** |  | [optional] 
**skipped** | **int** |  | [optional] 
**total_after** | **int** |  | [optional] 
**prompts_available** | **int** |  | [optional] 
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


