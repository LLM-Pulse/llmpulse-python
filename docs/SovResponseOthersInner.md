# SovResponseOthersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rank** | **int** |  | [optional] 
**actor** | [**Actor**](Actor.md) |  | [optional] 
**share** | **float** |  | [optional] 

## Example

```python
from llmpulse.models.sov_response_others_inner import SovResponseOthersInner

# TODO update the JSON string below
json = "{}"
# create an instance of SovResponseOthersInner from a JSON string
sov_response_others_inner_instance = SovResponseOthersInner.from_json(json)
# print the JSON string representation of the object
print(SovResponseOthersInner.to_json())

# convert the object into a dict
sov_response_others_inner_dict = sov_response_others_inner_instance.to_dict()
# create an instance of SovResponseOthersInner from a dict
sov_response_others_inner_from_dict = SovResponseOthersInner.from_dict(sov_response_others_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


