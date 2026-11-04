# CmsSite


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **str** |  | [optional] 
**site_url** | **str** | The site address as connected | [optional] 
**host** | **str** |  | [optional] 
**status** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.cms_site import CmsSite

# TODO update the JSON string below
json = "{}"
# create an instance of CmsSite from a JSON string
cms_site_instance = CmsSite.from_json(json)
# print the JSON string representation of the object
print(CmsSite.to_json())

# convert the object into a dict
cms_site_dict = cms_site_instance.to_dict()
# create an instance of CmsSite from a dict
cms_site_from_dict = CmsSite.from_dict(cms_site_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


