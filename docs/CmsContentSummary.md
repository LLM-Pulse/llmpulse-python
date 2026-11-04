# CmsContentSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | WordPress post or page id | [optional] 
**type** | **str** |  | [optional] 
**status** | **str** | WordPress status (publish, future, draft, pending or private) | [optional] 
**slug** | **str** |  | [optional] 
**title** | **str** | Plain-text title as the site renders it | [optional] 
**url** | **str** | The public link on the connected site; null when the site names a link on another host | [optional] 
**modified_at** | **datetime** |  | [optional] 

## Example

```python
from llmpulse.models.cms_content_summary import CmsContentSummary

# TODO update the JSON string below
json = "{}"
# create an instance of CmsContentSummary from a JSON string
cms_content_summary_instance = CmsContentSummary.from_json(json)
# print the JSON string representation of the object
print(CmsContentSummary.to_json())

# convert the object into a dict
cms_content_summary_dict = cms_content_summary_instance.to_dict()
# create an instance of CmsContentSummary from a dict
cms_content_summary_from_dict = CmsContentSummary.from_dict(cms_content_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


