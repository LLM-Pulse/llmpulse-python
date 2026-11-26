# CompetitorCitationsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[CompetitorCitationRecord]**](CompetitorCitationRecord.md) |  | 

## Example

```python
from llmpulse.models.competitor_citations_response import CompetitorCitationsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorCitationsResponse from a JSON string
competitor_citations_response_instance = CompetitorCitationsResponse.from_json(json)
# print the JSON string representation of the object
print(CompetitorCitationsResponse.to_json())

# convert the object into a dict
competitor_citations_response_dict = competitor_citations_response_instance.to_dict()
# create an instance of CompetitorCitationsResponse from a dict
competitor_citations_response_from_dict = CompetitorCitationsResponse.from_dict(competitor_citations_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


