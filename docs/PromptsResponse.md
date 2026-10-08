# PromptsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[PromptRecord]**](PromptRecord.md) |  | 

## Example

```python
from llmpulse.models.prompts_response import PromptsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PromptsResponse from a JSON string
prompts_response_instance = PromptsResponse.from_json(json)
# print the JSON string representation of the object
print(PromptsResponse.to_json())

# convert the object into a dict
prompts_response_dict = prompts_response_instance.to_dict()
# create an instance of PromptsResponse from a dict
prompts_response_from_dict = PromptsResponse.from_dict(prompts_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


