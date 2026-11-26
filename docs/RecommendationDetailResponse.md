# RecommendationDetailResponse

One recommendation run with its items

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**project_id** | **int** |  | 
**recommendation_type** | **str** |  | 
**status** | **str** |  | 
**error_message** | **str** | Set only when status is failed | 
**generated_at** | **datetime** | Null until the generation completes | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**total_recommendations** | **int** |  | 
**high_priority_count** | **int** |  | 
**summary** | [**RecommendationDetailResponseSummary**](RecommendationDetailResponseSummary.md) |  | 
**context** | **object** | Generation context and run diagnostics as stored; empty until the generation completes. Its keys are not a stable contract | 
**report_data** | **Dict[str, object]** | The stored run, including the evidence indices (prompts_index, citations_index, own_content_index and others) that the source_refs codes of the items point to. Its keys are not a stable contract | 
**item_counts** | [**RecommendationDetailResponseItemCounts**](RecommendationDetailResponseItemCounts.md) |  | 
**items** | [**List[RecommendationItem]**](RecommendationItem.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.recommendation_detail_response import RecommendationDetailResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RecommendationDetailResponse from a JSON string
recommendation_detail_response_instance = RecommendationDetailResponse.from_json(json)
# print the JSON string representation of the object
print(RecommendationDetailResponse.to_json())

# convert the object into a dict
recommendation_detail_response_dict = recommendation_detail_response_instance.to_dict()
# create an instance of RecommendationDetailResponse from a dict
recommendation_detail_response_from_dict = RecommendationDetailResponse.from_dict(recommendation_detail_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


