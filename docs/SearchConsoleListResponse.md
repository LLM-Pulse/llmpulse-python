# SearchConsoleListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**var_property** | [**SearchConsoleProperty**](SearchConsoleProperty.md) |  | [optional] 
**var_from** | **date** |  | [optional] 
**to** | **date** |  | [optional] 
**data_through** | **date** | Latest date Google has published for the property, or for every combined property (it lags 2-3 days). Later days are missing, not zero. | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** | Rows in this window (one Google request, at most 25,000) | [optional] 
**sort** | **str** |  | [optional] 
**start_row** | **int** | Present when start_row was set | [optional] 
**truncated** | **bool** | Present (true) when Google returned 25,000 rows, so more rows exist past this window | [optional] 
**data** | [**List[SearchConsoleListResponseDataInner]**](SearchConsoleListResponseDataInner.md) |  | [optional] 
**request_id** | **str** |  | [optional] 
**properties** | [**List[SearchConsoleProperty]**](SearchConsoleProperty.md) | With a list or all in the property parameter, the properties whose data the response holds (instead of property) | [optional] 
**excluded_properties** | [**List[SearchConsoleExcludedProperty]**](SearchConsoleExcludedProperty.md) | With a list or all, selected properties left out because another selected property already counts them | [optional] 
**property_errors** | [**List[SearchConsolePropertyError]**](SearchConsolePropertyError.md) | With a list or all, selected properties Google refused, left out of the figures | [optional] 

## Example

```python
from llmpulse.models.search_console_list_response import SearchConsoleListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleListResponse from a JSON string
search_console_list_response_instance = SearchConsoleListResponse.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleListResponse.to_json())

# convert the object into a dict
search_console_list_response_dict = search_console_list_response_instance.to_dict()
# create an instance of SearchConsoleListResponse from a dict
search_console_list_response_from_dict = SearchConsoleListResponse.from_dict(search_console_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


