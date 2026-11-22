# BingWebmasterTimeseriesResponse


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
**data_through** | **date** | The last day synced for the site. Later days are missing, not zero. | [optional] 
**granularity** | **str** |  | [optional] 
**data** | [**List[BingWebmasterTimeseriesResponseDataInner]**](BingWebmasterTimeseriesResponseDataInner.md) | One bucket per day, week (starting Monday) or month that has synced days. Days without data are left out, not reported as zero. | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.bing_webmaster_timeseries_response import BingWebmasterTimeseriesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BingWebmasterTimeseriesResponse from a JSON string
bing_webmaster_timeseries_response_instance = BingWebmasterTimeseriesResponse.from_json(json)
# print the JSON string representation of the object
print(BingWebmasterTimeseriesResponse.to_json())

# convert the object into a dict
bing_webmaster_timeseries_response_dict = bing_webmaster_timeseries_response_instance.to_dict()
# create an instance of BingWebmasterTimeseriesResponse from a dict
bing_webmaster_timeseries_response_from_dict = BingWebmasterTimeseriesResponse.from_dict(bing_webmaster_timeseries_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


