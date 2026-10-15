# PromptsImportRequestRowsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prompt** | **str** |  | 
**country_code** | **str** | ISO 3166-1 alpha-2 code or country name (default the project country) | [optional] 
**language_code** | **str** | ISO language code or language name (default the project language) | [optional] 
**tags** | **List[str]** | Tag names for this prompt, created when missing | [optional] 

## Example

```python
from llmpulse.models.prompts_import_request_rows_inner import PromptsImportRequestRowsInner

# TODO update the JSON string below
json = "{}"
# create an instance of PromptsImportRequestRowsInner from a JSON string
prompts_import_request_rows_inner_instance = PromptsImportRequestRowsInner.from_json(json)
# print the JSON string representation of the object
print(PromptsImportRequestRowsInner.to_json())

# convert the object into a dict
prompts_import_request_rows_inner_dict = prompts_import_request_rows_inner_instance.to_dict()
# create an instance of PromptsImportRequestRowsInner from a dict
prompts_import_request_rows_inner_from_dict = PromptsImportRequestRowsInner.from_dict(prompts_import_request_rows_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


