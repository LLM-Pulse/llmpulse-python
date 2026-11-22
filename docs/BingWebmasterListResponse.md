# BingWebmasterListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**site** | **str** | The connected site, as Bing Webmaster Tools names it (e.g. https://example.com/) | [optional] 
**sync_status** | **str** | State of the daily sync: pending, syncing, completed, failed or on_hold (the data already synced still answers, but stops updating until the site is reconnected) | [optional] 
**last_synced_at** | **datetime** | When the site last synced. Null before its first sync, or while history_current is false. | [optional] 
**history_current** | **bool** | False right after the site was changed and before its first sync. Until then data is empty and data_through is null. | [optional] 
**var_from** | **date** |  | [optional] 
**to** | **date** |  | [optional] 
**data_through** | **date** | The last week_ending synced for the site (the Friday that closes a Bing week) | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** | Distinct pages or queries found in the weeks of the window | [optional] 
**sort** | **str** |  | [optional] 
**weeks_covered** | **int** | Weeks with data whose week_ending falls in the window | [optional] 
**data** | [**List[BingWebmasterListResponseDataInner]**](BingWebmasterListResponseDataInner.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.bing_webmaster_list_response import BingWebmasterListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BingWebmasterListResponse from a JSON string
bing_webmaster_list_response_instance = BingWebmasterListResponse.from_json(json)
# print the JSON string representation of the object
print(BingWebmasterListResponse.to_json())

# convert the object into a dict
bing_webmaster_list_response_dict = bing_webmaster_list_response_instance.to_dict()
# create an instance of BingWebmasterListResponse from a dict
bing_webmaster_list_response_from_dict = BingWebmasterListResponse.from_dict(bing_webmaster_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


