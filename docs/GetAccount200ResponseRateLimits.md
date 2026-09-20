# GetAccount200ResponseRateLimits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requests_per_minute** | **int** | The ceiling enforced for the API key used on this call, which may be above the 300/min default. | [optional] 
**write_requests_per_minute** | **int** | Flat ceiling on write requests, the same for every key. | [optional] 

## Example

```python
from llmpulse.models.get_account200_response_rate_limits import GetAccount200ResponseRateLimits

# TODO update the JSON string below
json = "{}"
# create an instance of GetAccount200ResponseRateLimits from a JSON string
get_account200_response_rate_limits_instance = GetAccount200ResponseRateLimits.from_json(json)
# print the JSON string representation of the object
print(GetAccount200ResponseRateLimits.to_json())

# convert the object into a dict
get_account200_response_rate_limits_dict = get_account200_response_rate_limits_instance.to_dict()
# create an instance of GetAccount200ResponseRateLimits from a dict
get_account200_response_rate_limits_from_dict = GetAccount200ResponseRateLimits.from_dict(get_account200_response_rate_limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


