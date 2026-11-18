# UrlListEntryInput

An entry. A plain string is read as its value.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **str** | An exact URL, a \&quot;host/path/*\&quot; prefix or a domain. | 
**match_type** | **str** |  | [optional] 
**added_on** | **date** | When the URL was published or bought. Default today. | [optional] 
**cost** | **float** | What the URL cost, in the list currency. | [optional] 
**channel** | **str** | Where it came from, such as a marketplace or PR agency. | [optional] 

## Example

```python
from llmpulse.models.url_list_entry_input import UrlListEntryInput

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListEntryInput from a JSON string
url_list_entry_input_instance = UrlListEntryInput.from_json(json)
# print the JSON string representation of the object
print(UrlListEntryInput.to_json())

# convert the object into a dict
url_list_entry_input_dict = url_list_entry_input_instance.to_dict()
# create an instance of UrlListEntryInput from a dict
url_list_entry_input_from_dict = UrlListEntryInput.from_dict(url_list_entry_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


