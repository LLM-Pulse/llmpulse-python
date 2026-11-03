# SearchConsoleOpportunitiesResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **str** |  | [optional] 
**impressions** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** | 0..1 fraction | [optional] 
**position** | **float** | Impression-weighted average position | [optional] 
**potential_clicks** | **int** | Clicks a move into the top 3 would add at top_ctr (never negative); null when top_ctr is null | [optional] 

## Example

```python
from llmpulse.models.search_console_opportunities_response_data_inner import SearchConsoleOpportunitiesResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleOpportunitiesResponseDataInner from a JSON string
search_console_opportunities_response_data_inner_instance = SearchConsoleOpportunitiesResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleOpportunitiesResponseDataInner.to_json())

# convert the object into a dict
search_console_opportunities_response_data_inner_dict = search_console_opportunities_response_data_inner_instance.to_dict()
# create an instance of SearchConsoleOpportunitiesResponseDataInner from a dict
search_console_opportunities_response_data_inner_from_dict = SearchConsoleOpportunitiesResponseDataInner.from_dict(search_console_opportunities_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


