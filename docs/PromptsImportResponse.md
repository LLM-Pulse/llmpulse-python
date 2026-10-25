# PromptsImportResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**processed_rows** | **int** | Distinct rows imported or matched to an existing prompt | 
**created** | **int** |  | 
**duplicates** | **int** | Rows that matched an existing prompt (they still get the row&#39;s tags, unless a team member lacks update access to Prompts) | 
**tagged** | **int** | New prompt-tag links | 
**created_tags** | **int** |  | 
**row_errors** | [**List[PromptsImportResponseRowErrorsInner]**](PromptsImportResponseRowErrorsInner.md) | Rows that were skipped or whose tags were not added, by their index in rows | 
**length_warning** | **str** | Which tracked AI models will skip new prompts that are too long for them | 
**prompts_available** | **int** | Prompt slots left on the plan; null when unlimited | 
**tracked** | **bool** | Whether scheduled runs include the project the prompts were imported into. False when it is paused or beyond the plan&#39;s project limit, so the new prompts do not run until that changes | 
**untracked_reason** | **str** | Why tracked is false: paused or project_limit. Null when tracked | 
**warning** | **str** | What to do when tracked is false. Null when tracked | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.prompts_import_response import PromptsImportResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PromptsImportResponse from a JSON string
prompts_import_response_instance = PromptsImportResponse.from_json(json)
# print the JSON string representation of the object
print(PromptsImportResponse.to_json())

# convert the object into a dict
prompts_import_response_dict = prompts_import_response_instance.to_dict()
# create an instance of PromptsImportResponse from a dict
prompts_import_response_from_dict = PromptsImportResponse.from_dict(prompts_import_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


