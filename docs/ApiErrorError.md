# ApiErrorError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **str** |  | [optional] 
**message** | **str** |  | [optional] 
**meta** | **object** | Extra detail for some codes. A not-connected or access-revoked error from the Search Console, AI traffic, web analytics or agent traffic endpoints carries connect_url, the in-app page where the user connects or reconnects the source. | [optional] 

## Example

```python
from llmpulse.models.api_error_error import ApiErrorError

# TODO update the JSON string below
json = "{}"
# create an instance of ApiErrorError from a JSON string
api_error_error_instance = ApiErrorError.from_json(json)
# print the JSON string representation of the object
print(ApiErrorError.to_json())

# convert the object into a dict
api_error_error_dict = api_error_error_instance.to_dict()
# create an instance of ApiErrorError from a dict
api_error_error_from_dict = ApiErrorError.from_dict(api_error_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


