# AssignPromptTagsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**prompt_ids** | **List[int]** |  | 
**tag_ids** | **List[int]** |  | [optional] 
**tag_names** | **List[str]** |  | [optional] 
**create_missing** | **bool** |  | [optional] 

## Example

```python
from llmpulse.models.assign_prompt_tags_request import AssignPromptTagsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AssignPromptTagsRequest from a JSON string
assign_prompt_tags_request_instance = AssignPromptTagsRequest.from_json(json)
# print the JSON string representation of the object
print(AssignPromptTagsRequest.to_json())

# convert the object into a dict
assign_prompt_tags_request_dict = assign_prompt_tags_request_instance.to_dict()
# create an instance of AssignPromptTagsRequest from a dict
assign_prompt_tags_request_from_dict = AssignPromptTagsRequest.from_dict(assign_prompt_tags_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


