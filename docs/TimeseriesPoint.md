# TimeseriesPoint


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** | Calendar day in Europe/Madrid (YYYY-MM-DD). With granularity week or month it is the first day of the bucket (the Monday, or the 1st of the month). | [optional] 
**value** | **float** | Null when the metric has no value for the bucket, e.g. a rate, position or sentiment metric on a day without answers. | [optional] 

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


