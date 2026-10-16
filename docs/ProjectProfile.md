# ProjectProfile

The project name and profile, as PATCH /projects/{id} and the update_project MCP tool return them

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 
**brand_name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**industry** | **object** | Industry as stored: one key as a string (e.g. SAAS), or an array of key strings. Deliberately untyped so generated clients decode either shape | [optional] 
**business_model** | **str** |  | [optional] 
**business_model_other** | **str** | Set only when business_model is OTHER | [optional] 
**target_audience** | **str** |  | [optional] 
**primary_products** | **List[str]** |  | [optional] 
**brand_voice** | **str** |  | [optional] 
**goals** | **str** |  | [optional] 
**matching_names** | **List[str]** |  | 
**additional_owned_domains** | **List[str]** | Other domains the brand owns (at most 10, each a website&#39;s own domain covering its subdomains), whose citations count as owned like the project website. Empty when none | 
**prompt_limit** | **int** | Maximum number of active prompts this project may hold; null when only the account quota applies | 

## Example

```python
from llmpulse.models.project_profile import ProjectProfile

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectProfile from a JSON string
project_profile_instance = ProjectProfile.from_json(json)
# print the JSON string representation of the object
print(ProjectProfile.to_json())

# convert the object into a dict
project_profile_dict = project_profile_instance.to_dict()
# create an instance of ProjectProfile from a dict
project_profile_from_dict = ProjectProfile.from_dict(project_profile_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


