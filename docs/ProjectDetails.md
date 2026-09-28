# ProjectDetails


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** | Internal project label (sidebar, settings, admin) | [optional] 
**brand_name** | **str** | LLM-facing brand label (used in prompts and customer-facing charts). Defaults to &#x60;name&#x60; when not set. | [optional] 
**url** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**matching_names** | **List[str]** |  | [optional] 
**industry** | **object** | Industry as stored: one key as a string (e.g. SAAS), or an array of key strings when the project was created with a list or the in-app multi-select. Deliberately untyped so generated clients decode either shape | [optional] 
**business_model** | **str** |  | [optional] 
**business_model_other** | **str** | Set only when business_model is OTHER | [optional] 
**primary_products** | **List[str]** |  | [optional] 
**target_audience** | **str** |  | [optional] 
**brand_voice** | **str** |  | [optional] 
**goals** | **str** |  | [optional] 
**country_code** | **str** |  | [optional] 
**language_code** | **str** |  | [optional] 
**paused** | **bool** |  | [optional] 
**google_play_id** | **str** |  | [optional] 
**app_store_id** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**stats** | [**ProjectDetailsAllOfStats**](ProjectDetailsAllOfStats.md) |  | [optional] 

## Example

```python
from llmpulse.models.project_details import ProjectDetails

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDetails from a JSON string
project_details_instance = ProjectDetails.from_json(json)
# print the JSON string representation of the object
print(ProjectDetails.to_json())

# convert the object into a dict
project_details_dict = project_details_instance.to_dict()
# create an instance of ProjectDetails from a dict
project_details_from_dict = ProjectDetails.from_dict(project_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


