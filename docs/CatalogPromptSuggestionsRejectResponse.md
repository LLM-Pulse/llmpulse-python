# CatalogPromptSuggestionsRejectResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**rejected** | **int** |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.catalog_prompt_suggestions_reject_response import CatalogPromptSuggestionsRejectResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CatalogPromptSuggestionsRejectResponse from a JSON string
catalog_prompt_suggestions_reject_response_instance = CatalogPromptSuggestionsRejectResponse.from_json(json)
# print the JSON string representation of the object
print(CatalogPromptSuggestionsRejectResponse.to_json())

# convert the object into a dict
catalog_prompt_suggestions_reject_response_dict = catalog_prompt_suggestions_reject_response_instance.to_dict()
# create an instance of CatalogPromptSuggestionsRejectResponse from a dict
catalog_prompt_suggestions_reject_response_from_dict = CatalogPromptSuggestionsRejectResponse.from_dict(catalog_prompt_suggestions_reject_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


