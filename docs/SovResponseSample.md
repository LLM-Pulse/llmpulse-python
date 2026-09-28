# SovResponseSample

The period the current shares were computed on (the last one with mentions), same shape as a periods item; null when the window has no mentions.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** |  | [optional] 
**mentions** | **int** |  | [optional] 
**partial** | **bool** |  | [optional] 
**confidence** | **str** |  | [optional] 
**margin_of_error** | **float** |  | [optional] 

## Example

```python
from llmpulse.models.sov_response_sample import SovResponseSample

# TODO update the JSON string below
json = "{}"
# create an instance of SovResponseSample from a JSON string
sov_response_sample_instance = SovResponseSample.from_json(json)
# print the JSON string representation of the object
print(SovResponseSample.to_json())

# convert the object into a dict
sov_response_sample_dict = sov_response_sample_instance.to_dict()
# create an instance of SovResponseSample from a dict
sov_response_sample_from_dict = SovResponseSample.from_dict(sov_response_sample_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


