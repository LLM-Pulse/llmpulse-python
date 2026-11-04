# CmsContentItem


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
**excerpt** | **str** | Plain-text excerpt, up to 2,000 characters | [optional] 
**content_html** | **str** | Sanitized HTML (headings, paragraphs, lists, tables, quotes, code, links with href only), up to 200,000 characters | [optional] 
**content_truncated** | **bool** |  | [optional] 

## Example

```python
from llmpulse.models.cms_content_item import CmsContentItem

# TODO update the JSON string below
json = "{}"
# create an instance of CmsContentItem from a JSON string
cms_content_item_instance = CmsContentItem.from_json(json)
# print the JSON string representation of the object
print(CmsContentItem.to_json())

# convert the object into a dict
cms_content_item_dict = cms_content_item_instance.to_dict()
# create an instance of CmsContentItem from a dict
cms_content_item_from_dict = CmsContentItem.from_dict(cms_content_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


