# SearchConsoleSummaryResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**var_property** | [**SearchConsoleProperty**](SearchConsoleProperty.md) |  | [optional] 
**var_from** | **date** |  | [optional] 
**to** | **date** |  | [optional] 
**data_through** | **date** | Latest date Google has published for the property, or for every combined property (it lags 2-3 days). Later days are missing, not zero. | [optional] 
**totals** | [**SearchConsoleMetrics**](SearchConsoleMetrics.md) |  | [optional] 
**dimension** | **str** | Present when a breakdown was requested | [optional] 
**breakdown** | [**List[SearchConsoleSummaryResponseBreakdownInner]**](SearchConsoleSummaryResponseBreakdownInner.md) | Present when a breakdown was requested, sorted by impressions descending | [optional] 
**breakdown_truncated** | **bool** | Present (true) when limit or Google&#39;s 25,000-row maximum left breakdown rows out, so they add up to less than totals | [optional] 
**request_id** | **str** |  | [optional] 
**properties** | [**List[SearchConsoleProperty]**](SearchConsoleProperty.md) | With a list or all in the property parameter, the properties whose data the response holds (instead of property) | [optional] 
**excluded_properties** | [**List[SearchConsoleExcludedProperty]**](SearchConsoleExcludedProperty.md) | With a list or all, selected properties left out because another selected property already counts them | [optional] 
**property_errors** | [**List[SearchConsolePropertyError]**](SearchConsolePropertyError.md) | With a list or all, selected properties Google refused, left out of the figures | [optional] 

## Example

```python
from llmpulse.models.search_console_summary_response import SearchConsoleSummaryResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleSummaryResponse from a JSON string
search_console_summary_response_instance = SearchConsoleSummaryResponse.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleSummaryResponse.to_json())

# convert the object into a dict
search_console_summary_response_dict = search_console_summary_response_instance.to_dict()
# create an instance of SearchConsoleSummaryResponse from a dict
search_console_summary_response_from_dict = SearchConsoleSummaryResponse.from_dict(search_console_summary_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


