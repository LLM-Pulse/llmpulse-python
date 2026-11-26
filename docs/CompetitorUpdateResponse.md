# CompetitorUpdateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**competitor** | [**CompetitorUpdateResponseCompetitor**](CompetitorUpdateResponseCompetitor.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.competitor_update_response import CompetitorUpdateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorUpdateResponse from a JSON string
competitor_update_response_instance = CompetitorUpdateResponse.from_json(json)
# print the JSON string representation of the object
print(CompetitorUpdateResponse.to_json())

# convert the object into a dict
competitor_update_response_dict = competitor_update_response_instance.to_dict()
# create an instance of CompetitorUpdateResponse from a dict
competitor_update_response_from_dict = CompetitorUpdateResponse.from_dict(competitor_update_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


