# IntelligenceTaskCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**task_type** | **str** |  | 
**prompt_id** | **int** |  | [optional] 
**custom_topic** | **str** |  | [optional] 
**user_instructions** | **str** |  | [optional] 
**output_language_code** | **str** |  | [optional] 
**existing_content** | **str** |  | [optional] 
**existing_content_url** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.intelligence_task_create_request import IntelligenceTaskCreateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of IntelligenceTaskCreateRequest from a JSON string
intelligence_task_create_request_instance = IntelligenceTaskCreateRequest.from_json(json)
# print the JSON string representation of the object
print(IntelligenceTaskCreateRequest.to_json())

# convert the object into a dict
intelligence_task_create_request_dict = intelligence_task_create_request_instance.to_dict()
# create an instance of IntelligenceTaskCreateRequest from a dict
intelligence_task_create_request_from_dict = IntelligenceTaskCreateRequest.from_dict(intelligence_task_create_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


