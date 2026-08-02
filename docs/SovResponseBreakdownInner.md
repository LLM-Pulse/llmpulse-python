# SovResponseBreakdownInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rank** | **int** |  | [optional] 
**actor** | [**Actor**](Actor.md) |  | [optional] 
**share** | **float** |  | [optional] 
**others** | **bool** |  | [optional] 

## Example

```python
from llmpulse.models.sov_response_breakdown_inner import SovResponseBreakdownInner

# TODO update the JSON string below
json = "{}"
# create an instance of SovResponseBreakdownInner from a JSON string
sov_response_breakdown_inner_instance = SovResponseBreakdownInner.from_json(json)
# print the JSON string representation of the object
print(SovResponseBreakdownInner.to_json())

# convert the object into a dict
sov_response_breakdown_inner_dict = sov_response_breakdown_inner_instance.to_dict()
# create an instance of SovResponseBreakdownInner from a dict
sov_response_breakdown_inner_from_dict = SovResponseBreakdownInner.from_dict(sov_response_breakdown_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


