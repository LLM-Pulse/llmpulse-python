# SovResponseCurrentInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actor** | [**Actor**](Actor.md) |  | [optional] 
**share** | **float** |  | [optional] 
**previous_share** | **float** | The actor&#39;s share in the last complete bucket before the current one; null without complete history. | [optional] 
**avg_share** | **float** | Mean share across complete buckets with data (partial buckets excluded); null without complete history. | [optional] 

## Example

```python
from llmpulse.models.sov_response_current_inner import SovResponseCurrentInner

# TODO update the JSON string below
json = "{}"
# create an instance of SovResponseCurrentInner from a JSON string
sov_response_current_inner_instance = SovResponseCurrentInner.from_json(json)
# print the JSON string representation of the object
print(SovResponseCurrentInner.to_json())

# convert the object into a dict
sov_response_current_inner_dict = sov_response_current_inner_instance.to_dict()
# create an instance of SovResponseCurrentInner from a dict
sov_response_current_inner_from_dict = SovResponseCurrentInner.from_dict(sov_response_current_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


