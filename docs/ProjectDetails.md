# ProjectDetails


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** | Internal project label (sidebar, settings, admin) | [optional] 
**brand_name** | **str** | LLM-facing brand label (used in prompts and customer-facing charts). Null when not set, in which case prompts and charts use &#x60;name&#x60;. | [optional] 
**tracked** | **bool** | Whether scheduled runs include this project. False when it is paused, or when the plan&#39;s project limit leaves it out (the oldest projects up to the limit run), so its prompts do not run | 
**untracked_reason** | **str** | Why tracked is false: paused or project_limit. Null when tracked | 
**url** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**matching_names** | **List[str]** |  | [optional] 
**additional_owned_domains** | **List[str]** | Other domains the brand owns (at most 10, each a website&#39;s own domain covering its subdomains), whose citations count as owned like the project website. Empty when none | [optional] 
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
**prompt_limit** | **int** | The most prompts this project can hold, set by the account owner or a co-owner (Account Settings &gt; Prompt Limits). Null when the project has no limit of its own; the account&#39;s plan allowance applies either way | [optional] 
**stats** | [**ProjectDetailsAllOfStats**](ProjectDetailsAllOfStats.md) |  | [optional] 
**data_coverage** | [**ProjectDetailsAllOfDataCoverage**](ProjectDetailsAllOfDataCoverage.md) |  | [optional] 
**search_console** | [**ProjectDetailsAllOfSearchConsole**](ProjectDetailsAllOfSearchConsole.md) |  | [optional] 
**ai_traffic** | [**ProjectDetailsAllOfAiTraffic**](ProjectDetailsAllOfAiTraffic.md) |  | [optional] 
**agent_traffic** | [**ProjectDetailsAllOfAgentTraffic**](ProjectDetailsAllOfAgentTraffic.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

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


