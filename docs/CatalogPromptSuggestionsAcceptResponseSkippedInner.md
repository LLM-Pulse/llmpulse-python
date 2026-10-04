# CatalogPromptSuggestionsAcceptResponseSkippedInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**suggestion_id** | **int** |  | 
**reason** | **str** | accepted or rejected (the suggestion was no longer pending), or pending_deletion | 

## Example

```python
from llmpulse.models.catalog_prompt_suggestions_accept_response_skipped_inner import CatalogPromptSuggestionsAcceptResponseSkippedInner

# TODO update the JSON string below
json = "{}"
# create an instance of CatalogPromptSuggestionsAcceptResponseSkippedInner from a JSON string
catalog_prompt_suggestions_accept_response_skipped_inner_instance = CatalogPromptSuggestionsAcceptResponseSkippedInner.from_json(json)
# print the JSON string representation of the object
print(CatalogPromptSuggestionsAcceptResponseSkippedInner.to_json())

# convert the object into a dict
catalog_prompt_suggestions_accept_response_skipped_inner_dict = catalog_prompt_suggestions_accept_response_skipped_inner_instance.to_dict()
# create an instance of CatalogPromptSuggestionsAcceptResponseSkippedInner from a dict
catalog_prompt_suggestions_accept_response_skipped_inner_from_dict = CatalogPromptSuggestionsAcceptResponseSkippedInner.from_dict(catalog_prompt_suggestions_accept_response_skipped_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


