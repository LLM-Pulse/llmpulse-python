# LocalBusinessesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**totals** | [**LocalBusinessesTotals**](LocalBusinessesTotals.md) |  | [optional] 
**data** | [**List[LocalBusiness]**](LocalBusiness.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.local_businesses_response import LocalBusinessesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of LocalBusinessesResponse from a JSON string
local_businesses_response_instance = LocalBusinessesResponse.from_json(json)
# print the JSON string representation of the object
print(LocalBusinessesResponse.to_json())

# convert the object into a dict
local_businesses_response_dict = local_businesses_response_instance.to_dict()
# create an instance of LocalBusinessesResponse from a dict
local_businesses_response_from_dict = LocalBusinessesResponse.from_dict(local_businesses_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


