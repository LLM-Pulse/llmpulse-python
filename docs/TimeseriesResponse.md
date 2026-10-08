# TimeseriesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**var_from** | **datetime** |  | [optional] 
**to** | **datetime** |  | [optional] 
**granularity** | **str** | day, week or month | [optional] 
**filters** | [**MetricsFiltersEcho**](MetricsFiltersEcho.md) |  | [optional] 
**series** | **Dict[str, List[TimeseriesSeries]]** |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.timeseries_response import TimeseriesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TimeseriesResponse from a JSON string
timeseries_response_instance = TimeseriesResponse.from_json(json)
# print the JSON string representation of the object
print(TimeseriesResponse.to_json())

# convert the object into a dict
timeseries_response_dict = timeseries_response_instance.to_dict()
# create an instance of TimeseriesResponse from a dict
timeseries_response_from_dict = TimeseriesResponse.from_dict(timeseries_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


