# TimeseriesPoint


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **datetime** |  | [optional] 
**value** | **float** |  | [optional] 

## Example

```python
from llmpulse.models.timeseries_point import TimeseriesPoint

# TODO update the JSON string below
json = "{}"
# create an instance of TimeseriesPoint from a JSON string
timeseries_point_instance = TimeseriesPoint.from_json(json)
# print the JSON string representation of the object
print(TimeseriesPoint.to_json())

# convert the object into a dict
timeseries_point_dict = timeseries_point_instance.to_dict()
# create an instance of TimeseriesPoint from a dict
timeseries_point_from_dict = TimeseriesPoint.from_dict(timeseries_point_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


