# PromptsImportRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**rows** | [**List[PromptsImportRequestRowsInner]**](PromptsImportRequestRowsInner.md) | One object per prompt (max 500) | 

## Example

```python
from llmpulse.models.prompts_import_request import PromptsImportRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PromptsImportRequest from a JSON string
prompts_import_request_instance = PromptsImportRequest.from_json(json)
# print the JSON string representation of the object
print(PromptsImportRequest.to_json())

# convert the object into a dict
prompts_import_request_dict = prompts_import_request_instance.to_dict()
# create an instance of PromptsImportRequest from a dict
prompts_import_request_from_dict = PromptsImportRequest.from_dict(prompts_import_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


