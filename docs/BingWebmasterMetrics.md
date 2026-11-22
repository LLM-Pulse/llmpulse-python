# BingWebmasterMetrics

Bing reports no average position in its daily totals.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**impressions** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** | 0..1 fraction | [optional] 

## Example

```python
from llmpulse.models.bing_webmaster_metrics import BingWebmasterMetrics

# TODO update the JSON string below
json = "{}"
# create an instance of BingWebmasterMetrics from a JSON string
bing_webmaster_metrics_instance = BingWebmasterMetrics.from_json(json)
# print the JSON string representation of the object
print(BingWebmasterMetrics.to_json())

# convert the object into a dict
bing_webmaster_metrics_dict = bing_webmaster_metrics_instance.to_dict()
# create an instance of BingWebmasterMetrics from a dict
bing_webmaster_metrics_from_dict = BingWebmasterMetrics.from_dict(bing_webmaster_metrics_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


