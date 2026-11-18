# UrlList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 
**description** | **str** |  | 
**currency** | **str** | The currency of the entry costs. | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.url_list import UrlList

# TODO update the JSON string below
json = "{}"
# create an instance of UrlList from a JSON string
url_list_instance = UrlList.from_json(json)
# print the JSON string representation of the object
print(UrlList.to_json())

# convert the object into a dict
url_list_dict = url_list_instance.to_dict()
# create an instance of UrlList from a dict
url_list_from_dict = UrlList.from_dict(url_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


