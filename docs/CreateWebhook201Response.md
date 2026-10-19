# CreateWebhook201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**project_id** | **int** |  | [optional] 
**event_type** | **str** |  | [optional] 
**target_url** | **str** |  | [optional] 
**disabled** | **bool** | True when the subscription receives no more events, including when the API key or OAuth connection that created it was revoked, or when that API key is limited to some projects and no longer covers the subscription&#39;s project. Creating it again with the same project, event and URL replaces it with a new subscription and secret. | [optional] 
**failure_count** | **int** |  | [optional] 
**last_delivered_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**secret** | **str** | HMAC signing secret (whsec_...). Returned when the subscription is created, and on a re-post only to the API key or OAuth connection that created it; absent for any other credential. | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.create_webhook201_response import CreateWebhook201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateWebhook201Response from a JSON string
create_webhook201_response_instance = CreateWebhook201Response.from_json(json)
# print the JSON string representation of the object
print(CreateWebhook201Response.to_json())

# convert the object into a dict
create_webhook201_response_dict = create_webhook201_response_instance.to_dict()
# create an instance of CreateWebhook201Response from a dict
create_webhook201_response_from_dict = CreateWebhook201Response.from_dict(create_webhook201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


