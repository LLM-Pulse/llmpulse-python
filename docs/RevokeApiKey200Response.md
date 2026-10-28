# RevokeApiKey200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**revoked** | **bool** |  | [optional] 
**id** | **int** |  | [optional] 
**revoked_at** | **datetime** |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.revoke_api_key200_response import RevokeApiKey200Response

# TODO update the JSON string below
json = "{}"
# create an instance of RevokeApiKey200Response from a JSON string
revoke_api_key200_response_instance = RevokeApiKey200Response.from_json(json)
# print the JSON string representation of the object
print(RevokeApiKey200Response.to_json())

# convert the object into a dict
revoke_api_key200_response_dict = revoke_api_key200_response_instance.to_dict()
# create an instance of RevokeApiKey200Response from a dict
revoke_api_key200_response_from_dict = RevokeApiKey200Response.from_dict(revoke_api_key200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


