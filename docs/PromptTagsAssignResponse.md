# PromptTagsAssignResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**prompts_targeted** | **int** | Prompts of the project among prompt_ids | 
**tags_attached** | [**List[TagRef]**](TagRef.md) |  | 
**new_links_created** | **int** |  | 
**skipped_already_linked** | **int** |  | 
**missing_tag_names** | **List[str]** | tag_names that matched no tag and were not created | 
**ignored_prompt_ids** | **List[int]** | prompt_ids that are not prompts of this project | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.prompt_tags_assign_response import PromptTagsAssignResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PromptTagsAssignResponse from a JSON string
prompt_tags_assign_response_instance = PromptTagsAssignResponse.from_json(json)
# print the JSON string representation of the object
print(PromptTagsAssignResponse.to_json())

# convert the object into a dict
prompt_tags_assign_response_dict = prompt_tags_assign_response_instance.to_dict()
# create an instance of PromptTagsAssignResponse from a dict
prompt_tags_assign_response_from_dict = PromptTagsAssignResponse.from_dict(prompt_tags_assign_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


