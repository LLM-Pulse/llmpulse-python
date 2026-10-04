# CatalogPromptSuggestionProduct

The catalog product the suggestion was written for

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**external_id** | **str** | The store&#39;s product id, e.g. gid://shopify/Product/1 | [optional] 
**handle** | **str** |  | [optional] 
**title** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.catalog_prompt_suggestion_product import CatalogPromptSuggestionProduct

# TODO update the JSON string below
json = "{}"
# create an instance of CatalogPromptSuggestionProduct from a JSON string
catalog_prompt_suggestion_product_instance = CatalogPromptSuggestionProduct.from_json(json)
# print the JSON string representation of the object
print(CatalogPromptSuggestionProduct.to_json())

# convert the object into a dict
catalog_prompt_suggestion_product_dict = catalog_prompt_suggestion_product_instance.to_dict()
# create an instance of CatalogPromptSuggestionProduct from a dict
catalog_prompt_suggestion_product_from_dict = CatalogPromptSuggestionProduct.from_dict(catalog_prompt_suggestion_product_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


