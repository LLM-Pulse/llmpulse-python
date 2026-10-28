# CreateApiKey201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 
**prefix** | **str** | The visible start of the token, to recognize the key. Never the secret itself. | 
**scope** | **str** |  | 
**project_scoped** | **bool** | True when the key is limited to project_ids; false for an account-wide key. | 
**project_ids** | **List[int]** | The projects the key is limited to; empty for an account-wide key. | 
**created_at** | **datetime** |  | 
**last_used_at** | **datetime** | Updated at most once a minute. | 
**revoked_at** | **datetime** |  | 
**token** | **str** | The secret to send as Bearer token. Shown only in this response. | 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.create_api_key201_response import CreateApiKey201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateApiKey201Response from a JSON string
create_api_key201_response_instance = CreateApiKey201Response.from_json(json)
# print the JSON string representation of the object
print(CreateApiKey201Response.to_json())

# convert the object into a dict
create_api_key201_response_dict = create_api_key201_response_instance.to_dict()
# create an instance of CreateApiKey201Response from a dict
create_api_key201_response_from_dict = CreateApiKey201Response.from_dict(create_api_key201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


