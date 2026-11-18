# UrlListInvalidEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **str** |  | 
**reason** | **str** |  | 
**message** | **str** |  | 

## Example

```python
from llmpulse.models.url_list_invalid_entry import UrlListInvalidEntry

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListInvalidEntry from a JSON string
url_list_invalid_entry_instance = UrlListInvalidEntry.from_json(json)
# print the JSON string representation of the object
print(UrlListInvalidEntry.to_json())

# convert the object into a dict
url_list_invalid_entry_dict = url_list_invalid_entry_instance.to_dict()
# create an instance of UrlListInvalidEntry from a dict
url_list_invalid_entry_from_dict = UrlListInvalidEntry.from_dict(url_list_invalid_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


