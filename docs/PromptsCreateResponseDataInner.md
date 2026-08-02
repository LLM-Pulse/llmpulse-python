# PromptsCreateResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**raw_input** | **str** |  | [optional] 
**status** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.prompts_create_response_data_inner import PromptsCreateResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of PromptsCreateResponseDataInner from a JSON string
prompts_create_response_data_inner_instance = PromptsCreateResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(PromptsCreateResponseDataInner.to_json())

# convert the object into a dict
prompts_create_response_data_inner_dict = prompts_create_response_data_inner_instance.to_dict()
# create an instance of PromptsCreateResponseDataInner from a dict
prompts_create_response_data_inner_from_dict = PromptsCreateResponseDataInner.from_dict(prompts_create_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


