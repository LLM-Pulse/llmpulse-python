# BingWebmasterSummaryResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**site** | **str** | The connected site, as Bing Webmaster Tools names it (e.g. https://example.com/) | [optional] 
**sync_status** | **str** | State of the daily sync: pending, syncing, completed, failed or on_hold. on_hold means Bing refused the stored API key or the site is no longer verified: the data already synced still answers but stops updating until the site is reconnected in Preferences &gt; Project Settings &gt; Connections. | [optional] 
**last_synced_at** | **datetime** | When the site last synced. Null before its first sync, or while history_current is false. | [optional] 
**history_current** | **bool** | False right after the site was changed and before its first sync. Until then the response holds no data and data_through is null. | [optional] 
**var_from** | **date** |  | [optional] 
**to** | **date** |  | [optional] 
**data_through** | **date** | The last day synced for the site. Later days are missing, not zero. | [optional] 
**totals** | [**BingWebmasterMetrics**](BingWebmasterMetrics.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.bing_webmaster_summary_response import BingWebmasterSummaryResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BingWebmasterSummaryResponse from a JSON string
bing_webmaster_summary_response_instance = BingWebmasterSummaryResponse.from_json(json)
# print the JSON string representation of the object
print(BingWebmasterSummaryResponse.to_json())

# convert the object into a dict
bing_webmaster_summary_response_dict = bing_webmaster_summary_response_instance.to_dict()
# create an instance of BingWebmasterSummaryResponse from a dict
bing_webmaster_summary_response_from_dict = BingWebmasterSummaryResponse.from_dict(bing_webmaster_summary_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


