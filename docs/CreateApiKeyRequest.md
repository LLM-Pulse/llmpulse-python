# CreateApiKeyRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | A label to recognize the key, for example the customer it is for | 
**scope** | **str** | read (default) only reads data; read_write can also create, change and delete within the key&#39;s projects | [optional] [default to 'read']
**project_ids** | **List[int]** | The projects the key is limited to, at least one | 

## Example

```python
from llmpulse.models.create_api_key_request import CreateApiKeyRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateApiKeyRequest from a JSON string
create_api_key_request_instance = CreateApiKeyRequest.from_json(json)
# print the JSON string representation of the object
print(CreateApiKeyRequest.to_json())

# convert the object into a dict
create_api_key_request_dict = create_api_key_request_instance.to_dict()
# create an instance of CreateApiKeyRequest from a dict
create_api_key_request_from_dict = CreateApiKeyRequest.from_dict(create_api_key_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


