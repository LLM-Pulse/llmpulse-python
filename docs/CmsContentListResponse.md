# CmsContentListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**site** | [**CmsSite**](CmsSite.md) |  | [optional] 
**type** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**total_pages** | **int** |  | [optional] 
**data** | [**List[CmsContentSummary]**](CmsContentSummary.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.cms_content_list_response import CmsContentListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CmsContentListResponse from a JSON string
cms_content_list_response_instance = CmsContentListResponse.from_json(json)
# print the JSON string representation of the object
print(CmsContentListResponse.to_json())

# convert the object into a dict
cms_content_list_response_dict = cms_content_list_response_instance.to_dict()
# create an instance of CmsContentListResponse from a dict
cms_content_list_response_from_dict = CmsContentListResponse.from_dict(cms_content_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


