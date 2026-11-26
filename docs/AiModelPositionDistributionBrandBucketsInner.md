# AiModelPositionDistributionBrandBucketsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | 
**label** | **str** |  | 
**color** | **str** | Hex color the app charts the bucket with | 
**total** | **int** | Mentions in the bucket over the window | 
**data** | [**List[AiModelPositionDistributionBrandBucketsInnerDataInner]**](AiModelPositionDistributionBrandBucketsInnerDataInner.md) | One point per period of the window, oldest first, 0 included | 

## Example

```python
from llmpulse.models.ai_model_position_distribution_brand_buckets_inner import AiModelPositionDistributionBrandBucketsInner

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelPositionDistributionBrandBucketsInner from a JSON string
ai_model_position_distribution_brand_buckets_inner_instance = AiModelPositionDistributionBrandBucketsInner.from_json(json)
# print the JSON string representation of the object
print(AiModelPositionDistributionBrandBucketsInner.to_json())

# convert the object into a dict
ai_model_position_distribution_brand_buckets_inner_dict = ai_model_position_distribution_brand_buckets_inner_instance.to_dict()
# create an instance of AiModelPositionDistributionBrandBucketsInner from a dict
ai_model_position_distribution_brand_buckets_inner_from_dict = AiModelPositionDistributionBrandBucketsInner.from_dict(ai_model_position_distribution_brand_buckets_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


