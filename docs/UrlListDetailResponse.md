# UrlListDetailResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**url_list** | [**UrlList**](UrlList.md) |  | 
**filters** | [**UrlListFilters**](UrlListFilters.md) |  | 
**summary** | [**UrlListSummary**](UrlListSummary.md) |  | 
**status_counts** | [**UrlListStatusCounts**](UrlListStatusCounts.md) |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** |  | 
**entries** | [**List[UrlListEntry]**](UrlListEntry.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.url_list_detail_response import UrlListDetailResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListDetailResponse from a JSON string
url_list_detail_response_instance = UrlListDetailResponse.from_json(json)
# print the JSON string representation of the object
print(UrlListDetailResponse.to_json())

# convert the object into a dict
url_list_detail_response_dict = url_list_detail_response_instance.to_dict()
# create an instance of UrlListDetailResponse from a dict
url_list_detail_response_from_dict = UrlListDetailResponse.from_dict(url_list_detail_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


