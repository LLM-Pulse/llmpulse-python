# CatalogPromptSuggestionsAcceptResponseAcceptedInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**suggestion_id** | **int** |  | 
**prompt_id** | **int** |  | 
**collection_id** | **int** | The collection named after the product; null when the product has no title or the team member cannot create tags | 

## Example

```python
from llmpulse.models.catalog_prompt_suggestions_accept_response_accepted_inner import CatalogPromptSuggestionsAcceptResponseAcceptedInner

# TODO update the JSON string below
json = "{}"
# create an instance of CatalogPromptSuggestionsAcceptResponseAcceptedInner from a JSON string
catalog_prompt_suggestions_accept_response_accepted_inner_instance = CatalogPromptSuggestionsAcceptResponseAcceptedInner.from_json(json)
# print the JSON string representation of the object
print(CatalogPromptSuggestionsAcceptResponseAcceptedInner.to_json())

# convert the object into a dict
catalog_prompt_suggestions_accept_response_accepted_inner_dict = catalog_prompt_suggestions_accept_response_accepted_inner_instance.to_dict()
# create an instance of CatalogPromptSuggestionsAcceptResponseAcceptedInner from a dict
catalog_prompt_suggestions_accept_response_accepted_inner_from_dict = CatalogPromptSuggestionsAcceptResponseAcceptedInner.from_dict(catalog_prompt_suggestions_accept_response_accepted_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


