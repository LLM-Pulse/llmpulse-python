# TimeseriesSeries


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actor** | [**Actor**](Actor.md) |  | [optional] 
**metric** | **str** |  | [optional] 
**data** | [**List[TimeseriesPoint]**](TimeseriesPoint.md) |  | [optional] 

## Example

```python
from llmpulse.models.timeseries_series import TimeseriesSeries

# TODO update the JSON string below
json = "{}"
# create an instance of TimeseriesSeries from a JSON string
timeseries_series_instance = TimeseriesSeries.from_json(json)
# print the JSON string representation of the object
print(TimeseriesSeries.to_json())

# convert the object into a dict
timeseries_series_dict = timeseries_series_instance.to_dict()
# create an instance of TimeseriesSeries from a dict
timeseries_series_from_dict = TimeseriesSeries.from_dict(timeseries_series_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


