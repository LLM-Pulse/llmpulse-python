# ProjectDetailsAllOfPitchRun

The one run of a pitch project; null for a tracked project. Its answers are dated between launched_at and settled_at, so read its metrics with from set to the launched_at date (the default ranges leave out a pitch older than a few weeks)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** | starting before the run begins, running while answers arrive, ready once every AI model has answered or stopped trying | [optional] 
**launched_at** | **datetime** |  | [optional] 
**settled_at** | **datetime** |  | [optional] 
**models** | **List[str]** | The AI models the run asks, fixed when it starts | [optional] 
**answers_expected** | **int** |  | [optional] 
**answers_received** | **int** |  | [optional] 

## Example

```python
from llmpulse.models.project_details_all_of_pitch_run import ProjectDetailsAllOfPitchRun

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDetailsAllOfPitchRun from a JSON string
project_details_all_of_pitch_run_instance = ProjectDetailsAllOfPitchRun.from_json(json)
# print the JSON string representation of the object
print(ProjectDetailsAllOfPitchRun.to_json())

# convert the object into a dict
project_details_all_of_pitch_run_dict = project_details_all_of_pitch_run_instance.to_dict()
# create an instance of ProjectDetailsAllOfPitchRun from a dict
project_details_all_of_pitch_run_from_dict = ProjectDetailsAllOfPitchRun.from_dict(project_details_all_of_pitch_run_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


