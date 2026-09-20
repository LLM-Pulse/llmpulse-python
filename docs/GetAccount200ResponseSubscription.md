# GetAccount200ResponseSubscription

Billing state. Present only for callers who can access Billing and Plans in the app; absent otherwise.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**trialing** | **bool** |  | [optional] 
**current_period_ends_at** | **datetime** |  | [optional] 

## Example

```python
from llmpulse.models.get_account200_response_subscription import GetAccount200ResponseSubscription

# TODO update the JSON string below
json = "{}"
# create an instance of GetAccount200ResponseSubscription from a JSON string
get_account200_response_subscription_instance = GetAccount200ResponseSubscription.from_json(json)
# print the JSON string representation of the object
print(GetAccount200ResponseSubscription.to_json())

# convert the object into a dict
get_account200_response_subscription_dict = get_account200_response_subscription_instance.to_dict()
# create an instance of GetAccount200ResponseSubscription from a dict
get_account200_response_subscription_from_dict = GetAccount200ResponseSubscription.from_dict(get_account200_response_subscription_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


