# CmsContentItemResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**site** | [**CmsSite**](CmsSite.md) |  | [optional] 
**data** | [**CmsContentItem**](CmsContentItem.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.cms_content_item_response import CmsContentItemResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CmsContentItemResponse from a JSON string
cms_content_item_response_instance = CmsContentItemResponse.from_json(json)
# print the JSON string representation of the object
print(CmsContentItemResponse.to_json())

# convert the object into a dict
cms_content_item_response_dict = cms_content_item_response_instance.to_dict()
# create an instance of CmsContentItemResponse from a dict
cms_content_item_response_from_dict = CmsContentItemResponse.from_dict(cms_content_item_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


