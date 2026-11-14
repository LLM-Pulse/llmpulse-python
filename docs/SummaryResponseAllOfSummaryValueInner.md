# SummaryResponseAllOfSummaryValueInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actor** | [**Actor**](Actor.md) |  | [optional] 
**metric** | **str** |  | [optional] 
**total** | **float** | Count metrics sum the buckets; rate, position and sentiment metrics average them. ai_visibility_score (weighted_visibility) is the window&#39;s points divided by its data days (the days with responses under the filters), the number the app shows, whatever the granularity. | [optional] 
**aggregation** | **str** | How total combines the buckets (average for ai_visibility_score, a per-data-day score) | [optional] 
**min** | **float** |  | [optional] 
**max** | **float** |  | [optional] 
**last** | **float** |  | [optional] 

## Example

```python
from llmpulse.models.summary_response_all_of_summary_value_inner import SummaryResponseAllOfSummaryValueInner

# TODO update the JSON string below
json = "{}"
# create an instance of SummaryResponseAllOfSummaryValueInner from a JSON string
summary_response_all_of_summary_value_inner_instance = SummaryResponseAllOfSummaryValueInner.from_json(json)
# print the JSON string representation of the object
print(SummaryResponseAllOfSummaryValueInner.to_json())

# convert the object into a dict
summary_response_all_of_summary_value_inner_dict = summary_response_all_of_summary_value_inner_instance.to_dict()
# create an instance of SummaryResponseAllOfSummaryValueInner from a dict
summary_response_all_of_summary_value_inner_from_dict = SummaryResponseAllOfSummaryValueInner.from_dict(summary_response_all_of_summary_value_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


