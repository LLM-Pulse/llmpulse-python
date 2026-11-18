# UrlListEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**value** | **str** | The exact URL, \&quot;host/path\&quot; of a prefix, or the host of a domain rule. | 
**match_type** | **str** |  | 
**host** | **str** |  | 
**status** | **str** |  | 
**added_on** | **date** |  | 
**cost** | **float** |  | 
**channel** | **str** |  | 
**citations** | **int** |  | 
**cited_pages** | **int** |  | 
**first_cited_at** | **datetime** |  | 
**last_cited_at** | **datetime** |  | 
**days_to_first_citation** | **int** |  | 
**avg_citation_position** | **float** |  | 
**models** | **List[str]** |  | 
**brand_mentioned** | **bool** |  | 

## Example

```python
from llmpulse.models.url_list_entry import UrlListEntry

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListEntry from a JSON string
url_list_entry_instance = UrlListEntry.from_json(json)
# print the JSON string representation of the object
print(UrlListEntry.to_json())

# convert the object into a dict
url_list_entry_dict = url_list_entry_instance.to_dict()
# create an instance of UrlListEntry from a dict
url_list_entry_from_dict = UrlListEntry.from_dict(url_list_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


