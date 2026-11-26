# StudiesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Studies matching the filters across every page | 
**data** | [**List[StudySummary]**](StudySummary.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.studies_response import StudiesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of StudiesResponse from a JSON string
studies_response_instance = StudiesResponse.from_json(json)
# print the JSON string representation of the object
print(StudiesResponse.to_json())

# convert the object into a dict
studies_response_dict = studies_response_instance.to_dict()
# create an instance of StudiesResponse from a dict
studies_response_from_dict = StudiesResponse.from_dict(studies_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


