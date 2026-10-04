# CatalogPromptSuggestionsCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**platform** | **str** |  | 
**country_code** | **str** | Defaults to the project country | [optional] 
**language_code** | **str** | Defaults to the project language | [optional] 
**products** | [**List[CatalogProduct]**](CatalogProduct.md) |  | 

## Example

```python
from llmpulse.models.catalog_prompt_suggestions_create_request import CatalogPromptSuggestionsCreateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CatalogPromptSuggestionsCreateRequest from a JSON string
catalog_prompt_suggestions_create_request_instance = CatalogPromptSuggestionsCreateRequest.from_json(json)
# print the JSON string representation of the object
print(CatalogPromptSuggestionsCreateRequest.to_json())

# convert the object into a dict
catalog_prompt_suggestions_create_request_dict = catalog_prompt_suggestions_create_request_instance.to_dict()
# create an instance of CatalogPromptSuggestionsCreateRequest from a dict
catalog_prompt_suggestions_create_request_from_dict = CatalogPromptSuggestionsCreateRequest.from_dict(catalog_prompt_suggestions_create_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


