# UrlListWithStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 
**description** | **str** |  | 
**currency** | **str** | The currency of the entry costs. | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**entries_count** | **int** |  | 
**cited_entries** | **int** | Entries an AI answer cited in the window. | 
**citations** | **int** | AI answers citing any entry in the window, each once. | 
**last_cited_at** | **datetime** | The latest answer citing an entry, up to the window&#39;s end. | 

## Example

```python
from llmpulse.models.url_list_with_stats import UrlListWithStats

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListWithStats from a JSON string
url_list_with_stats_instance = UrlListWithStats.from_json(json)
# print the JSON string representation of the object
print(UrlListWithStats.to_json())

# convert the object into a dict
url_list_with_stats_dict = url_list_with_stats_instance.to_dict()
# create an instance of UrlListWithStats from a dict
url_list_with_stats_from_dict = UrlListWithStats.from_dict(url_list_with_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


