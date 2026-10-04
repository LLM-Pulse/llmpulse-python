# CatalogPromptSuggestion


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**prompt** | **str** |  | 
**status** | **str** | pending, accepted or rejected | 
**source** | **str** | Always catalog | 
**country_code** | **str** |  | 
**language_code** | **str** |  | 
**product** | [**CatalogPromptSuggestionProduct**](CatalogPromptSuggestionProduct.md) |  | 
**prompt_id** | **int** | The tracked prompt an accepted suggestion became; null until accepted | 
**accepted_at** | **datetime** | When the suggestion was accepted; null until then | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.catalog_prompt_suggestion import CatalogPromptSuggestion

# TODO update the JSON string below
json = "{}"
# create an instance of CatalogPromptSuggestion from a JSON string
catalog_prompt_suggestion_instance = CatalogPromptSuggestion.from_json(json)
# print the JSON string representation of the object
print(CatalogPromptSuggestion.to_json())

# convert the object into a dict
catalog_prompt_suggestion_dict = catalog_prompt_suggestion_instance.to_dict()
# create an instance of CatalogPromptSuggestion from a dict
catalog_prompt_suggestion_from_dict = CatalogPromptSuggestion.from_dict(catalog_prompt_suggestion_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


