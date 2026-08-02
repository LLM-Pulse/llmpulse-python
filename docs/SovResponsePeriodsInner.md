# SovResponsePeriodsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** |  | [optional] 
**mentions** | **int** |  | [optional] 
**partial** | **bool** |  | [optional] 

## Example

```python
from llmpulse.models.sov_response_periods_inner import SovResponsePeriodsInner

# TODO update the JSON string below
json = "{}"
# create an instance of SovResponsePeriodsInner from a JSON string
sov_response_periods_inner_instance = SovResponsePeriodsInner.from_json(json)
# print the JSON string representation of the object
print(SovResponsePeriodsInner.to_json())

# convert the object into a dict
sov_response_periods_inner_dict = sov_response_periods_inner_instance.to_dict()
# create an instance of SovResponsePeriodsInner from a dict
sov_response_periods_inner_from_dict = SovResponsePeriodsInner.from_dict(sov_response_periods_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


