# PromptsCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**prompts** | **List[str]** | Prompt texts (max 100). Each can be up to 2,000 bytes of UTF-8 text (about 2,000 characters in English, fewer with accented letters or non-Latin scripts). A new prompt over that returns ERR_INVALID_PARAM with error.meta.reason prompt_too_long and creates none of the batch; a text the project already tracks still comes back as exists. | 
**country_code** | **str** |  | 
**language_code** | **str** |  | 

## Example

```python
from llmpulse.models.prompts_create_request import PromptsCreateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PromptsCreateRequest from a JSON string
prompts_create_request_instance = PromptsCreateRequest.from_json(json)
# print the JSON string representation of the object
print(PromptsCreateRequest.to_json())

# convert the object into a dict
prompts_create_request_dict = prompts_create_request_instance.to_dict()
# create an instance of PromptsCreateRequest from a dict
prompts_create_request_from_dict = PromptsCreateRequest.from_dict(prompts_create_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


