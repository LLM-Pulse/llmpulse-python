# LocalesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**countries** | **List[str]** | Country codes with data | 
**languages** | **List[str]** | Language codes with data | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.locales_response import LocalesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of LocalesResponse from a JSON string
locales_response_instance = LocalesResponse.from_json(json)
# print the JSON string representation of the object
print(LocalesResponse.to_json())

# convert the object into a dict
locales_response_dict = locales_response_instance.to_dict()
# create an instance of LocalesResponse from a dict
locales_response_from_dict = LocalesResponse.from_dict(locales_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


