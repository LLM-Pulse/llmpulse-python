# SovResponsePeriodsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** |  | [optional] 
**mentions** | **int** |  | [optional] 
**partial** | **bool** |  | [optional] 
**confidence** | **str** | How far the shares of this period can be trusted, from its mentions: none (0), low (under 30), medium (under 100) or high (100 or more). | [optional] 
**margin_of_error** | **float** | Worst-case 95% margin of a share in percentage points, 98 / sqrt(mentions); mentions within one answer are not independent, so the real margin is at least this wide. null with no mentions. | [optional] 

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


