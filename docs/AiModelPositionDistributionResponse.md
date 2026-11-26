# AiModelPositionDistributionResponse

The positions at which one or two brands were mentioned, in four buckets, per period of the window.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**var_from** | **datetime** |  | 
**to** | **datetime** |  | 
**filters** | [**AiModelInsightsReportFiltersEcho**](AiModelInsightsReportFiltersEcho.md) |  | 
**granularity** | **str** |  | 
**brands** | [**List[AiModelPositionDistributionBrand]**](AiModelPositionDistributionBrand.md) | The first brand (brand1, else the project) and the second (brand2, else the competitor with the most mentions, else the project), each left out when it has no mention in the window | 
**max_stacked_value** | **int** | The largest mentions count of one period across the brands, for a shared chart axis | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.ai_model_position_distribution_response import AiModelPositionDistributionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelPositionDistributionResponse from a JSON string
ai_model_position_distribution_response_instance = AiModelPositionDistributionResponse.from_json(json)
# print the JSON string representation of the object
print(AiModelPositionDistributionResponse.to_json())

# convert the object into a dict
ai_model_position_distribution_response_dict = ai_model_position_distribution_response_instance.to_dict()
# create an instance of AiModelPositionDistributionResponse from a dict
ai_model_position_distribution_response_from_dict = AiModelPositionDistributionResponse.from_dict(ai_model_position_distribution_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


