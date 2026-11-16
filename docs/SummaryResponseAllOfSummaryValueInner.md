# SummaryResponseAllOfSummaryValueInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actor** | [**Actor**](Actor.md) |  | [optional] 
**metric** | **str** |  | [optional] 
**total** | **float** | Count metrics sum the buckets. Rate, position and sentiment metrics pool the whole window, the number the app shows for the same filters, whatever the granularity; visibility is all mentions over all responses x 100, citation_rate all citations over all responses x 100, a sentiment share all verdicts of that kind over all verdicts x 100, an average position the average of every position recorded in the window. They are never a mean of the bucket values. ai_visibility_score (weighted_visibility) is the window&#39;s points divided by its tracking runs (the days, weeks or months at the account&#39;s tracking frequency with responses under the filters). | [optional] 
**aggregation** | **str** | How total combines the buckets. sum for counts; average for rates, positions and sentiment, pooled over the window, and for ai_visibility_score, a per-run score | [optional] 
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


