# BingWebmasterListResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | The page URL or the query | [optional] 
**impressions** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** | 0..1 fraction | [optional] 
**avg_impression_position** | **float** | Average position when shown, weighted by impressions (lower is better) | [optional] 
**avg_click_position** | **float** | Average position when clicked, weighted by clicks. Null without clicks. | [optional] 

## Example

```python
from llmpulse.models.bing_webmaster_list_response_data_inner import BingWebmasterListResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of BingWebmasterListResponseDataInner from a JSON string
bing_webmaster_list_response_data_inner_instance = BingWebmasterListResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(BingWebmasterListResponseDataInner.to_json())

# convert the object into a dict
bing_webmaster_list_response_data_inner_dict = bing_webmaster_list_response_data_inner_instance.to_dict()
# create an instance of BingWebmasterListResponseDataInner from a dict
bing_webmaster_list_response_data_inner_from_dict = BingWebmasterListResponseDataInner.from_dict(bing_webmaster_list_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


