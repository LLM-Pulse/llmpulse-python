# GetAccount200ResponseLimits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prompts** | [**AccountQuota**](AccountQuota.md) |  | [optional] 
**projects** | [**AccountQuota**](AccountQuota.md) |  | [optional] 
**competitors_per_project** | [**AccountCapacity**](AccountCapacity.md) |  | [optional] 
**intelligence_tasks** | [**AccountQuota**](AccountQuota.md) |  | [optional] 
**team_members** | [**AccountCapacity**](AccountCapacity.md) |  | [optional] 
**recurring_geo_audits** | [**AccountQuota**](AccountQuota.md) |  | [optional] 
**geo_audit_manual_runs** | [**AccountQuota**](AccountQuota.md) |  | [optional] 

## Example

```python
from llmpulse.models.get_account200_response_limits import GetAccount200ResponseLimits

# TODO update the JSON string below
json = "{}"
# create an instance of GetAccount200ResponseLimits from a JSON string
get_account200_response_limits_instance = GetAccount200ResponseLimits.from_json(json)
# print the JSON string representation of the object
print(GetAccount200ResponseLimits.to_json())

# convert the object into a dict
get_account200_response_limits_dict = get_account200_response_limits_instance.to_dict()
# create an instance of GetAccount200ResponseLimits from a dict
get_account200_response_limits_from_dict = GetAccount200ResponseLimits.from_dict(get_account200_response_limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


