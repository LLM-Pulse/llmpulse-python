# PromptGenerationResponseError

Why a failed run failed

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **str** | ERR_GENERATION_FAILED, ERR_NOT_FOUND (no suggestions came back), ERR_QUOTA_EXCEEDED, or a Search Console error code | 
**message** | **str** |  | 

## Example

```python
from llmpulse.models.prompt_generation_response_error import PromptGenerationResponseError

# TODO update the JSON string below
json = "{}"
# create an instance of PromptGenerationResponseError from a JSON string
prompt_generation_response_error_instance = PromptGenerationResponseError.from_json(json)
# print the JSON string representation of the object
print(PromptGenerationResponseError.to_json())

# convert the object into a dict
prompt_generation_response_error_dict = prompt_generation_response_error_instance.to_dict()
# create an instance of PromptGenerationResponseError from a dict
prompt_generation_response_error_from_dict = PromptGenerationResponseError.from_dict(prompt_generation_response_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


