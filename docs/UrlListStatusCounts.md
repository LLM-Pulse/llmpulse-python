# UrlListStatusCounts


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cited** | **int** |  | 
**lost** | **int** |  | 
**not_cited** | **int** |  | 

## Example

```python
from llmpulse.models.url_list_status_counts import UrlListStatusCounts

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListStatusCounts from a JSON string
url_list_status_counts_instance = UrlListStatusCounts.from_json(json)
# print the JSON string representation of the object
print(UrlListStatusCounts.to_json())

# convert the object into a dict
url_list_status_counts_dict = url_list_status_counts_instance.to_dict()
# create an instance of UrlListStatusCounts from a dict
url_list_status_counts_from_dict = UrlListStatusCounts.from_dict(url_list_status_counts_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


