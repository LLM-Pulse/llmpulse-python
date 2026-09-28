# SovResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**periods** | [**List[SovResponsePeriodsInner]**](SovResponsePeriodsInner.md) | Per-bucket sample size and completeness: mentions is the total the shares were computed on (1-3 mentions produce the 100/50/33.33 low-sample patterns); partial marks buckets still collecting data or clipped by the requested window; confidence and margin_of_error read the sample size. | [optional] 
**sample** | [**SovResponseSample**](SovResponseSample.md) |  | [optional] 
**over_time** | [**List[SovResponseOverTimeInner]**](SovResponseOverTimeInner.md) |  | [optional] 
**current** | [**List[SovResponseCurrentInner]**](SovResponseCurrentInner.md) |  | [optional] 
**breakdown** | [**List[SovResponseBreakdownInner]**](SovResponseBreakdownInner.md) |  | [optional] 
**others** | **List[object]** |  | [optional] 

## Example

```python
from llmpulse.models.sov_response import SovResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SovResponse from a JSON string
sov_response_instance = SovResponse.from_json(json)
# print the JSON string representation of the object
print(SovResponse.to_json())

# convert the object into a dict
sov_response_dict = sov_response_instance.to_dict()
# create an instance of SovResponse from a dict
sov_response_from_dict = SovResponse.from_dict(sov_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


