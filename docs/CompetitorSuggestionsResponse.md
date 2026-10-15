# CompetitorSuggestionsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**basis** | **str** |  | 
**discovery** | [**CompetitorDiscoveryState**](CompetitorDiscoveryState.md) |  | 
**data** | [**List[CompetitorSuggestion]**](CompetitorSuggestion.md) |  | 

## Example

```python
from llmpulse.models.competitor_suggestions_response import CompetitorSuggestionsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorSuggestionsResponse from a JSON string
competitor_suggestions_response_instance = CompetitorSuggestionsResponse.from_json(json)
# print the JSON string representation of the object
print(CompetitorSuggestionsResponse.to_json())

# convert the object into a dict
competitor_suggestions_response_dict = competitor_suggestions_response_instance.to_dict()
# create an instance of CompetitorSuggestionsResponse from a dict
competitor_suggestions_response_from_dict = CompetitorSuggestionsResponse.from_dict(competitor_suggestions_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


