# SearchConsoleOpportunitiesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**var_property** | [**SearchConsoleProperty**](SearchConsoleProperty.md) |  | [optional] 
**properties** | [**List[SearchConsoleProperty]**](SearchConsoleProperty.md) | With a list or all in the property parameter, the properties whose data the response holds (instead of property) | [optional] 
**excluded_properties** | [**List[SearchConsoleExcludedProperty]**](SearchConsoleExcludedProperty.md) | With a list or all, selected properties left out because another selected property already counts them | [optional] 
**property_errors** | [**List[SearchConsolePropertyError]**](SearchConsolePropertyError.md) | With a list or all, selected properties Google refused, left out of the figures | [optional] 
**var_from** | **date** |  | [optional] 
**to** | **date** |  | [optional] 
**data_through** | **date** | Latest date Google has published for the property, or for every combined property (it lags 2-3 days). Later days are missing, not zero. | [optional] 
**min_impressions** | **int** |  | [optional] 
**min_position** | **float** |  | [optional] 
**max_position** | **float** |  | [optional] 
**top_ctr** | **float** | CTR (0..1) of the property&#39;s queries averaging position 3 or better in the window; null when there are none, and then no potential_clicks | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** | Rows in the report before paging | [optional] 
**truncated** | **bool** | Present (true) when Google returned its 25,000-row maximum for a property, so the report covers its top rows only | [optional] 
**data** | [**List[SearchConsoleOpportunitiesResponseDataInner]**](SearchConsoleOpportunitiesResponseDataInner.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.search_console_opportunities_response import SearchConsoleOpportunitiesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleOpportunitiesResponse from a JSON string
search_console_opportunities_response_instance = SearchConsoleOpportunitiesResponse.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleOpportunitiesResponse.to_json())

# convert the object into a dict
search_console_opportunities_response_dict = search_console_opportunities_response_instance.to_dict()
# create an instance of SearchConsoleOpportunitiesResponse from a dict
search_console_opportunities_response_from_dict = SearchConsoleOpportunitiesResponse.from_dict(search_console_opportunities_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


