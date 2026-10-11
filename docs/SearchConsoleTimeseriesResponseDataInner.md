# SearchConsoleTimeseriesResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** |  | [optional] 
**impressions** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** | 0..1 fraction | [optional] 
**position** | **float** | Impression-weighted average position | [optional] 

## Example

```python
from llmpulse.models.search_console_timeseries_response_data_inner import SearchConsoleTimeseriesResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleTimeseriesResponseDataInner from a JSON string
search_console_timeseries_response_data_inner_instance = SearchConsoleTimeseriesResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleTimeseriesResponseDataInner.to_json())

# convert the object into a dict
search_console_timeseries_response_data_inner_dict = search_console_timeseries_response_data_inner_instance.to_dict()
# create an instance of SearchConsoleTimeseriesResponseDataInner from a dict
search_console_timeseries_response_data_inner_from_dict = SearchConsoleTimeseriesResponseDataInner.from_dict(search_console_timeseries_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


