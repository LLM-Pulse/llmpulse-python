# AiModelPositionDistributionBrand


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | project or competitor | 
**id** | **int** | Project id, or competitor id | 
**competitor_id** | **int** | Null for the project, the competitor id otherwise | 
**name** | **str** |  | 
**domain** | **str** | Bare (scheme-less) domain. Null for the project when it has no URL. | 
**buckets** | [**List[AiModelPositionDistributionBrandBucketsInner]**](AiModelPositionDistributionBrandBucketsInner.md) | One per position bucket, in order: position_1, position_2_3, position_4_7 and position_8_plus | 
**max_stacked_value** | **int** | The brand&#39;s largest mentions count of one period, its buckets added up | 

## Example

```python
from llmpulse.models.ai_model_position_distribution_brand import AiModelPositionDistributionBrand

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelPositionDistributionBrand from a JSON string
ai_model_position_distribution_brand_instance = AiModelPositionDistributionBrand.from_json(json)
# print the JSON string representation of the object
print(AiModelPositionDistributionBrand.to_json())

# convert the object into a dict
ai_model_position_distribution_brand_dict = ai_model_position_distribution_brand_instance.to_dict()
# create an instance of AiModelPositionDistributionBrand from a dict
ai_model_position_distribution_brand_from_dict = AiModelPositionDistributionBrand.from_dict(ai_model_position_distribution_brand_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


