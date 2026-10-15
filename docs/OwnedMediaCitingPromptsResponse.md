# OwnedMediaCitingPromptsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**provider** | **str** |  | [optional] 
**var_from** | **datetime** |  | [optional] 
**to** | **datetime** |  | [optional] 
**item** | [**OwnedMediaCitedItem**](OwnedMediaCitedItem.md) |  | [optional] 
**citation_count** | **int** | Citations of the item in the window | [optional] 
**prompt_count** | **int** | Distinct prompts whose answers cited it | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** | Citing answers | [optional] 
**data** | [**List[OwnedMediaCitingAnswer]**](OwnedMediaCitingAnswer.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_citing_prompts_response import OwnedMediaCitingPromptsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaCitingPromptsResponse from a JSON string
owned_media_citing_prompts_response_instance = OwnedMediaCitingPromptsResponse.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaCitingPromptsResponse.to_json())

# convert the object into a dict
owned_media_citing_prompts_response_dict = owned_media_citing_prompts_response_instance.to_dict()
# create an instance of OwnedMediaCitingPromptsResponse from a dict
owned_media_citing_prompts_response_from_dict = OwnedMediaCitingPromptsResponse.from_dict(owned_media_citing_prompts_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


