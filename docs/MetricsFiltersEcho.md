# MetricsFiltersEcho

The filters the response was computed with, as the server resolved them. Each endpoint echoes only the keys it reads; a filter that was not given comes back null (or an empty list).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metrics** | **List[str]** | Requested metrics after alias resolution (mention_rate is echoed as visibility) | [optional] 
**granularity** | **str** | day, week or month | [optional] 
**model** | **str** | The model filter, or null when absent or not enabled for the account | [optional] 
**collection_id** | **str** | The collection_id parameter as sent (one id or a comma-separated list) | [optional] 
**collection_ids** | **List[int]** |  | [optional] 
**domains** | **List[str]** |  | [optional] 
**country_code** | **str** | Comma-separated country codes | [optional] 
**language_code** | **str** | Comma-separated language codes | [optional] 
**prompt** | **int** | The prompt id filter | [optional] 
**prompt_type** | **str** | Comma-separated prompt types | [optional] 
**brand_kind** | **str** |  | [optional] 
**competitors** | **List[int]** | Competitor ids from the competitors parameter; empty when it was not given | [optional] 
**include_project** | **bool** |  | [optional] 
**query** | **str** | Only present when a query filter was given | [optional] 

## Example

```python
from llmpulse.models.metrics_filters_echo import MetricsFiltersEcho

# TODO update the JSON string below
json = "{}"
# create an instance of MetricsFiltersEcho from a JSON string
metrics_filters_echo_instance = MetricsFiltersEcho.from_json(json)
# print the JSON string representation of the object
print(MetricsFiltersEcho.to_json())

# convert the object into a dict
metrics_filters_echo_dict = metrics_filters_echo_instance.to_dict()
# create an instance of MetricsFiltersEcho from a dict
metrics_filters_echo_from_dict = MetricsFiltersEcho.from_dict(metrics_filters_echo_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


