# RecommendationDetailResponseItemCounts

Items of the run per status, whatever item_status filters

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**active** | **int** |  | 
**completed** | **int** |  | 
**archived** | **int** |  | 

## Example

```python
from llmpulse.models.recommendation_detail_response_item_counts import RecommendationDetailResponseItemCounts

# TODO update the JSON string below
json = "{}"
# create an instance of RecommendationDetailResponseItemCounts from a JSON string
recommendation_detail_response_item_counts_instance = RecommendationDetailResponseItemCounts.from_json(json)
# print the JSON string representation of the object
print(RecommendationDetailResponseItemCounts.to_json())

# convert the object into a dict
recommendation_detail_response_item_counts_dict = recommendation_detail_response_item_counts_instance.to_dict()
# create an instance of RecommendationDetailResponseItemCounts from a dict
recommendation_detail_response_item_counts_from_dict = RecommendationDetailResponseItemCounts.from_dict(recommendation_detail_response_item_counts_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


