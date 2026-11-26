# PeecExportImportResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**import_id** | **int** |  | 
**status** | **str** | The import was accepted and finishes in the background | 
**prompts** | **int** | Distinct prompts of the file, per country and language; each becomes a tracked prompt of the project | 
**new_prompts** | **int** | The prompts the project does not hold yet, counted against the plan | 
**planned_answers** | **int** | Weekly answers the import files (prompts x tracked AI models x weeks) | 
**models** | **Dict[str, str]** | Each AI model name of the file that is imported, with the tracked AI model its answers are filed under | 
**skipped_models** | **List[str]** | AI model names of the file whose answers are skipped, because the account does not track them | 
**detected_brands** | **List[str]** | Brand names the export&#39;s mentions column lists (up to 50), none of them created as competitors | 
**app_url** | **str** | Opens the project&#39;s prompts in the app | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.peec_export_import_response import PeecExportImportResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PeecExportImportResponse from a JSON string
peec_export_import_response_instance = PeecExportImportResponse.from_json(json)
# print the JSON string representation of the object
print(PeecExportImportResponse.to_json())

# convert the object into a dict
peec_export_import_response_dict = peec_export_import_response_instance.to_dict()
# create an instance of PeecExportImportResponse from a dict
peec_export_import_response_from_dict = PeecExportImportResponse.from_dict(peec_export_import_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


