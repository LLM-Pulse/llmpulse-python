# CatalogPromptSuggestionsAcceptResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**accepted** | [**List[CatalogPromptSuggestionsAcceptResponseAcceptedInner]**](CatalogPromptSuggestionsAcceptResponseAcceptedInner.md) |  | 
**skipped** | [**List[CatalogPromptSuggestionsAcceptResponseSkippedInner]**](CatalogPromptSuggestionsAcceptResponseSkippedInner.md) |  | 
**prompts_available** | **int** | Prompt slots left on the plan; null when unlimited | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.catalog_prompt_suggestions_accept_response import CatalogPromptSuggestionsAcceptResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CatalogPromptSuggestionsAcceptResponse from a JSON string
catalog_prompt_suggestions_accept_response_instance = CatalogPromptSuggestionsAcceptResponse.from_json(json)
# print the JSON string representation of the object
print(CatalogPromptSuggestionsAcceptResponse.to_json())

# convert the object into a dict
catalog_prompt_suggestions_accept_response_dict = catalog_prompt_suggestions_accept_response_instance.to_dict()
# create an instance of CatalogPromptSuggestionsAcceptResponse from a dict
catalog_prompt_suggestions_accept_response_from_dict = CatalogPromptSuggestionsAcceptResponse.from_dict(catalog_prompt_suggestions_accept_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


