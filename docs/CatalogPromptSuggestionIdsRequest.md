# CatalogPromptSuggestionIdsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**ids** | **List[int]** |  | 

## Example

```python
from llmpulse.models.catalog_prompt_suggestion_ids_request import CatalogPromptSuggestionIdsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CatalogPromptSuggestionIdsRequest from a JSON string
catalog_prompt_suggestion_ids_request_instance = CatalogPromptSuggestionIdsRequest.from_json(json)
# print the JSON string representation of the object
print(CatalogPromptSuggestionIdsRequest.to_json())

# convert the object into a dict
catalog_prompt_suggestion_ids_request_dict = catalog_prompt_suggestion_ids_request_instance.to_dict()
# create an instance of CatalogPromptSuggestionIdsRequest from a dict
catalog_prompt_suggestion_ids_request_from_dict = CatalogPromptSuggestionIdsRequest.from_dict(catalog_prompt_suggestion_ids_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


