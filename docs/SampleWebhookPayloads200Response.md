# SampleWebhookPayloads200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_type** | **str** |  | [optional] 
**data** | [**List[SampleWebhookPayloads200ResponseDataInner]**](SampleWebhookPayloads200ResponseDataInner.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.sample_webhook_payloads200_response import SampleWebhookPayloads200Response

# TODO update the JSON string below
json = "{}"
# create an instance of SampleWebhookPayloads200Response from a JSON string
sample_webhook_payloads200_response_instance = SampleWebhookPayloads200Response.from_json(json)
# print the JSON string representation of the object
print(SampleWebhookPayloads200Response.to_json())

# convert the object into a dict
sample_webhook_payloads200_response_dict = sample_webhook_payloads200_response_instance.to_dict()
# create an instance of SampleWebhookPayloads200Response from a dict
sample_webhook_payloads200_response_from_dict = SampleWebhookPayloads200Response.from_dict(sample_webhook_payloads200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


