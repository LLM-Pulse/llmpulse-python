# BingWebmasterTimeseriesResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** | First day of the bucket | [optional] 
**impressions** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** | 0..1 fraction | [optional] 

## Example

```python
from llmpulse.models.bing_webmaster_timeseries_response_data_inner import BingWebmasterTimeseriesResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of BingWebmasterTimeseriesResponseDataInner from a JSON string
bing_webmaster_timeseries_response_data_inner_instance = BingWebmasterTimeseriesResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(BingWebmasterTimeseriesResponseDataInner.to_json())

# convert the object into a dict
bing_webmaster_timeseries_response_data_inner_dict = bing_webmaster_timeseries_response_data_inner_instance.to_dict()
# create an instance of BingWebmasterTimeseriesResponseDataInner from a dict
bing_webmaster_timeseries_response_data_inner_from_dict = BingWebmasterTimeseriesResponseDataInner.from_dict(bing_webmaster_timeseries_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


