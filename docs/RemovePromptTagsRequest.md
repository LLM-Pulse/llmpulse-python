# RemovePromptTagsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**prompt_ids** | **List[int]** |  | 
**tag_ids** | **List[int]** |  | [optional] 
**tag_names** | **List[str]** |  | [optional] 

## Example

```python
from llmpulse.models.remove_prompt_tags_request import RemovePromptTagsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RemovePromptTagsRequest from a JSON string
remove_prompt_tags_request_instance = RemovePromptTagsRequest.from_json(json)
# print the JSON string representation of the object
print(RemovePromptTagsRequest.to_json())

# convert the object into a dict
remove_prompt_tags_request_dict = remove_prompt_tags_request_instance.to_dict()
# create an instance of RemovePromptTagsRequest from a dict
remove_prompt_tags_request_from_dict = RemovePromptTagsRequest.from_dict(remove_prompt_tags_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


