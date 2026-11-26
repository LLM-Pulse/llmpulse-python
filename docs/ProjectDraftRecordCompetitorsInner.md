# ProjectDraftRecordCompetitorsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **str** |  | 
**brand_name** | **str** | Empty when the step sent none | 
**matching_names** | **List[str]** |  | 

## Example

```python
from llmpulse.models.project_draft_record_competitors_inner import ProjectDraftRecordCompetitorsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDraftRecordCompetitorsInner from a JSON string
project_draft_record_competitors_inner_instance = ProjectDraftRecordCompetitorsInner.from_json(json)
# print the JSON string representation of the object
print(ProjectDraftRecordCompetitorsInner.to_json())

# convert the object into a dict
project_draft_record_competitors_inner_dict = project_draft_record_competitors_inner_instance.to_dict()
# create an instance of ProjectDraftRecordCompetitorsInner from a dict
project_draft_record_competitors_inner_from_dict = ProjectDraftRecordCompetitorsInner.from_dict(project_draft_record_competitors_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


