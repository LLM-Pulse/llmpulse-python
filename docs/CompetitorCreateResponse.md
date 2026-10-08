# CompetitorCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**competitor** | [**CompetitorCreateResponseCompetitor**](CompetitorCreateResponseCompetitor.md) |  | 
**competitors_remaining** | **int** | Competitors the plan still allows in this project; null when unlimited | 
**total_competitors** | **int** |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.competitor_create_response import CompetitorCreateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorCreateResponse from a JSON string
competitor_create_response_instance = CompetitorCreateResponse.from_json(json)
# print the JSON string representation of the object
print(CompetitorCreateResponse.to_json())

# convert the object into a dict
competitor_create_response_dict = competitor_create_response_instance.to_dict()
# create an instance of CompetitorCreateResponse from a dict
competitor_create_response_from_dict = CompetitorCreateResponse.from_dict(competitor_create_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


