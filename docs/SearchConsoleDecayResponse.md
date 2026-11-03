# SearchConsoleDecayResponse


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
**dimension** | **str** |  | [optional] 
**compared_through** | **date** | Last day of the requested window that is compared, to or the last day Google has published when that is earlier | [optional] 
**previous_from** | **date** | Start of the window compared against, the same length as from..compared_through and just before it | [optional] 
**previous_to** | **date** |  | [optional] 
**min_clicks** | **int** |  | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** | Rows in the report before paging | [optional] 
**truncated** | **bool** | Present (true) when Google returned its 25,000-row maximum for a property, so the report covers its top rows only | [optional] 
**data** | [**List[SearchConsoleDecayResponseDataInner]**](SearchConsoleDecayResponseDataInner.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.search_console_decay_response import SearchConsoleDecayResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleDecayResponse from a JSON string
search_console_decay_response_instance = SearchConsoleDecayResponse.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleDecayResponse.to_json())

# convert the object into a dict
search_console_decay_response_dict = search_console_decay_response_instance.to_dict()
# create an instance of SearchConsoleDecayResponse from a dict
search_console_decay_response_from_dict = SearchConsoleDecayResponse.from_dict(search_console_decay_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


