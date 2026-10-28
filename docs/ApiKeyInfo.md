# ApiKeyInfo


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

## Example

```python
from llmpulse.models.api_key_info import ApiKeyInfo

# TODO update the JSON string below
json = "{}"
# create an instance of ApiKeyInfo from a JSON string
api_key_info_instance = ApiKeyInfo.from_json(json)
# print the JSON string representation of the object
print(ApiKeyInfo.to_json())

# convert the object into a dict
api_key_info_dict = api_key_info_instance.to_dict()
# create an instance of ApiKeyInfo from a dict
api_key_info_from_dict = ApiKeyInfo.from_dict(api_key_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


