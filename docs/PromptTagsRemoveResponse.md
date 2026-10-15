# PromptTagsRemoveResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**prompts_targeted** | **int** | Prompts of the project among prompt_ids | 
**tags_detached** | [**List[TagRef]**](TagRef.md) |  | 
**links_removed** | **int** |  | 
**skipped_not_linked** | **int** |  | 
**missing_tag_names** | **List[str]** | tag_names that matched no tag | 
**ignored_prompt_ids** | **List[int]** | prompt_ids that are not prompts of this project | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.prompt_tags_remove_response import PromptTagsRemoveResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PromptTagsRemoveResponse from a JSON string
prompt_tags_remove_response_instance = PromptTagsRemoveResponse.from_json(json)
# print the JSON string representation of the object
print(PromptTagsRemoveResponse.to_json())

# convert the object into a dict
prompt_tags_remove_response_dict = prompt_tags_remove_response_instance.to_dict()
# create an instance of PromptTagsRemoveResponse from a dict
prompt_tags_remove_response_from_dict = PromptTagsRemoveResponse.from_dict(prompt_tags_remove_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


