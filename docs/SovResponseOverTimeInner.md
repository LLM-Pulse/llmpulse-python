# SovResponseOverTimeInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actor** | [**Actor**](Actor.md) |  | [optional] 
**data** | [**List[TimeseriesPoint]**](TimeseriesPoint.md) |  | [optional] 

## Example

```python
from llmpulse.models.sov_response_over_time_inner import SovResponseOverTimeInner

# TODO update the JSON string below
json = "{}"
# create an instance of SovResponseOverTimeInner from a JSON string
sov_response_over_time_inner_instance = SovResponseOverTimeInner.from_json(json)
# print the JSON string representation of the object
print(SovResponseOverTimeInner.to_json())

# convert the object into a dict
sov_response_over_time_inner_dict = sov_response_over_time_inner_instance.to_dict()
# create an instance of SovResponseOverTimeInner from a dict
sov_response_over_time_inner_from_dict = SovResponseOverTimeInner.from_dict(sov_response_over_time_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


