# CatalogPromptSuggestionsCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**created** | **int** |  | 
**skipped** | **int** | Generated prompts not saved because the project already holds them as a suggestion (from any source or product, in any status). | 
**data** | [**List[CatalogPromptSuggestion]**](CatalogPromptSuggestion.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.catalog_prompt_suggestions_create_response import CatalogPromptSuggestionsCreateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CatalogPromptSuggestionsCreateResponse from a JSON string
catalog_prompt_suggestions_create_response_instance = CatalogPromptSuggestionsCreateResponse.from_json(json)
# print the JSON string representation of the object
print(CatalogPromptSuggestionsCreateResponse.to_json())

# convert the object into a dict
catalog_prompt_suggestions_create_response_dict = catalog_prompt_suggestions_create_response_instance.to_dict()
# create an instance of CatalogPromptSuggestionsCreateResponse from a dict
catalog_prompt_suggestions_create_response_from_dict = CatalogPromptSuggestionsCreateResponse.from_dict(catalog_prompt_suggestions_create_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


