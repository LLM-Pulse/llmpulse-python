# SampleWebhookPayloads200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event** | **str** |  | [optional] 
**occurred_at** | **datetime** |  | [optional] 
**project_id** | **int** |  | [optional] 
**subscription_id** | **int** |  | [optional] 
**data** | **object** |  | [optional] 

## Example

```python
from llmpulse.models.sample_webhook_payloads200_response_data_inner import SampleWebhookPayloads200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of SampleWebhookPayloads200ResponseDataInner from a JSON string
sample_webhook_payloads200_response_data_inner_instance = SampleWebhookPayloads200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(SampleWebhookPayloads200ResponseDataInner.to_json())

# convert the object into a dict
sample_webhook_payloads200_response_data_inner_dict = sample_webhook_payloads200_response_data_inner_instance.to_dict()
# create an instance of SampleWebhookPayloads200ResponseDataInner from a dict
sample_webhook_payloads200_response_data_inner_from_dict = SampleWebhookPayloads200ResponseDataInner.from_dict(sample_webhook_payloads200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


