# ProjectDetailsAllOfStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prompts_count** | **int** |  | [optional] 
**prompts_by_brand_kind** | [**ProjectDetailsAllOfStatsPromptsByBrandKind**](ProjectDetailsAllOfStatsPromptsByBrandKind.md) |  | [optional] 
**competitors_count** | **int** |  | [optional] 
**collections_count** | **int** |  | [optional] 

## Example

```python
from llmpulse.models.project_details_all_of_stats import ProjectDetailsAllOfStats

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDetailsAllOfStats from a JSON string
project_details_all_of_stats_instance = ProjectDetailsAllOfStats.from_json(json)
# print the JSON string representation of the object
print(ProjectDetailsAllOfStats.to_json())

# convert the object into a dict
project_details_all_of_stats_dict = project_details_all_of_stats_instance.to_dict()
# create an instance of ProjectDetailsAllOfStats from a dict
project_details_all_of_stats_from_dict = ProjectDetailsAllOfStats.from_dict(project_details_all_of_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


