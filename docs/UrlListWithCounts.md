# UrlListWithCounts


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

## Example

```python
from llmpulse.models.url_list_with_counts import UrlListWithCounts

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListWithCounts from a JSON string
url_list_with_counts_instance = UrlListWithCounts.from_json(json)
# print the JSON string representation of the object
print(UrlListWithCounts.to_json())

# convert the object into a dict
url_list_with_counts_dict = url_list_with_counts_instance.to_dict()
# create an instance of UrlListWithCounts from a dict
url_list_with_counts_from_dict = UrlListWithCounts.from_dict(url_list_with_counts_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


