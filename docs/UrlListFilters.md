# UrlListFilters

The filters the numbers were read with.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model** | **str** |  | [optional] 
**collection_id** | **str** |  | [optional] 
**country_code** | **str** |  | [optional] 
**language_code** | **str** |  | [optional] 
**prompt** | **int** |  | [optional] 
**brand_kind** | **str** |  | [optional] 
**var_from** | **str** |  | [optional] 
**to** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.url_list_filters import UrlListFilters

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListFilters from a JSON string
url_list_filters_instance = UrlListFilters.from_json(json)
# print the JSON string representation of the object
print(UrlListFilters.to_json())

# convert the object into a dict
url_list_filters_dict = url_list_filters_instance.to_dict()
# create an instance of UrlListFilters from a dict
url_list_filters_from_dict = UrlListFilters.from_dict(url_list_filters_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


