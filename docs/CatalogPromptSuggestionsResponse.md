# CatalogPromptSuggestionsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** |  | 
**data** | [**List[CatalogPromptSuggestion]**](CatalogPromptSuggestion.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.catalog_prompt_suggestions_response import CatalogPromptSuggestionsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CatalogPromptSuggestionsResponse from a JSON string
catalog_prompt_suggestions_response_instance = CatalogPromptSuggestionsResponse.from_json(json)
# print the JSON string representation of the object
print(CatalogPromptSuggestionsResponse.to_json())

# convert the object into a dict
catalog_prompt_suggestions_response_dict = catalog_prompt_suggestions_response_instance.to_dict()
# create an instance of CatalogPromptSuggestionsResponse from a dict
catalog_prompt_suggestions_response_from_dict = CatalogPromptSuggestionsResponse.from_dict(catalog_prompt_suggestions_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


