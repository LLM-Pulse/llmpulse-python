# IntelligenceTasksResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[IntelligenceTaskSummary]**](IntelligenceTaskSummary.md) |  | 

## Example

```python
from llmpulse.models.intelligence_tasks_response import IntelligenceTasksResponse

# TODO update the JSON string below
json = "{}"
# create an instance of IntelligenceTasksResponse from a JSON string
intelligence_tasks_response_instance = IntelligenceTasksResponse.from_json(json)
# print the JSON string representation of the object
print(IntelligenceTasksResponse.to_json())

# convert the object into a dict
intelligence_tasks_response_dict = intelligence_tasks_response_instance.to_dict()
# create an instance of IntelligenceTasksResponse from a dict
intelligence_tasks_response_from_dict = IntelligenceTasksResponse.from_dict(intelligence_tasks_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


