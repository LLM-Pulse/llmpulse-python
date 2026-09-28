# UpdateProjectRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Project name shown in the app. A label: it does not change mention detection unless brand_name is empty. Cannot be blank | [optional] 
**brand_name** | **str** | Brand name used to detect mentions. Applies to future runs; it does not rewrite history | [optional] 
**description** | **str** | What the brand does. Context for Recommendations and GEO Writer (Brand Book) | [optional] 
**industry** | **str** | Single industry key (e.g. SAAS), stored as sent; an array of keys is also accepted and stored as an array, like the in-app multi-select. Unknown keys are rejected with the valid keys listed | [optional] 
**business_model** | **str** | Business model key (e.g. B2B_SAAS); unknown keys are rejected | [optional] 
**business_model_other** | **str** | Free-text business model, only accepted when business_model is OTHER; rejected against any other key | [optional] 
**target_audience** | **str** | Who the brand sells to (Brand Book) | [optional] 
**brand_voice** | **str** | Tone of voice guidance for generated content (Brand Book) | [optional] 
**goals** | **str** | What the brand wants to achieve. Context for GEO Writer and prompt suggestions | [optional] 
**primary_products** | **List[str]** | Full replacement list of the main products or services | [optional] 
**matching_names** | **List[str]** | FULL replacement list of the brand-name variants used to detect mentions; send every variant to keep | [optional] 

## Example

```python
from llmpulse.models.update_project_request import UpdateProjectRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateProjectRequest from a JSON string
update_project_request_instance = UpdateProjectRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateProjectRequest.to_json())

# convert the object into a dict
update_project_request_dict = update_project_request_instance.to_dict()
# create an instance of UpdateProjectRequest from a dict
update_project_request_from_dict = UpdateProjectRequest.from_dict(update_project_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


