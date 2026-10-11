# SearchConsoleTimeseriesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**var_property** | [**SearchConsoleProperty**](SearchConsoleProperty.md) |  | [optional] 
**var_from** | **date** |  | [optional] 
**to** | **date** |  | [optional] 
**data_through** | **date** | Latest date Google has published for the property (it lags 2-3 days). Later days are missing, not zero. | [optional] 
**granularity** | **str** |  | [optional] 
**data** | [**List[SearchConsoleTimeseriesResponseDataInner]**](SearchConsoleTimeseriesResponseDataInner.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.search_console_timeseries_response import SearchConsoleTimeseriesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleTimeseriesResponse from a JSON string
search_console_timeseries_response_instance = SearchConsoleTimeseriesResponse.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleTimeseriesResponse.to_json())

# convert the object into a dict
search_console_timeseries_response_dict = search_console_timeseries_response_instance.to_dict()
# create an instance of SearchConsoleTimeseriesResponse from a dict
search_console_timeseries_response_from_dict = SearchConsoleTimeseriesResponse.from_dict(search_console_timeseries_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


