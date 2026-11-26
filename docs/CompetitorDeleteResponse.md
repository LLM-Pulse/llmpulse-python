# CompetitorDeleteResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**deleted** | **bool** | Always true | 
**id** | **int** |  | 
**brand_name** | **str** |  | 
**domain** | **str** |  | 
**total_competitors** | **int** | Competitors left in the project | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.competitor_delete_response import CompetitorDeleteResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorDeleteResponse from a JSON string
competitor_delete_response_instance = CompetitorDeleteResponse.from_json(json)
# print the JSON string representation of the object
print(CompetitorDeleteResponse.to_json())

# convert the object into a dict
competitor_delete_response_dict = competitor_delete_response_instance.to_dict()
# create an instance of CompetitorDeleteResponse from a dict
competitor_delete_response_from_dict = CompetitorDeleteResponse.from_dict(competitor_delete_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


