# CmsSendResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**created** | **bool** | false when this version had already been sent and the existing publication is returned | [optional] 
**publication** | [**CmsPublication**](CmsPublication.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.cms_send_response import CmsSendResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CmsSendResponse from a JSON string
cms_send_response_instance = CmsSendResponse.from_json(json)
# print the JSON string representation of the object
print(CmsSendResponse.to_json())

# convert the object into a dict
cms_send_response_dict = cms_send_response_instance.to_dict()
# create an instance of CmsSendResponse from a dict
cms_send_response_from_dict = CmsSendResponse.from_dict(cms_send_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


