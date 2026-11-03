# AiModelInsightsFiltersEcho

The filters the summary was computed with, as the server resolved them. A filter that was not given is left out, except granularity and competitors.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_from** | **datetime** |  | [optional] 
**to** | **datetime** |  | [optional] 
**granularity** | **str** | day, week or month; day when not given | [optional] 
**country_code** | **str** | Comma-separated country codes | [optional] 
**language_code** | **str** | Comma-separated language codes | [optional] 
**collection_id** | **str** | Comma-separated collection ids | [optional] 
**prompt_type** | **str** | Comma-separated prompt types | [optional] 
**brand_kind** | **str** |  | [optional] 
**competitors** | **List[int]** | Competitor ids from the competitors parameter; empty when it was not given | [optional] 

## Example

```python
from llmpulse.models.ai_model_insights_filters_echo import AiModelInsightsFiltersEcho

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelInsightsFiltersEcho from a JSON string
ai_model_insights_filters_echo_instance = AiModelInsightsFiltersEcho.from_json(json)
# print the JSON string representation of the object
print(AiModelInsightsFiltersEcho.to_json())

# convert the object into a dict
ai_model_insights_filters_echo_dict = ai_model_insights_filters_echo_instance.to_dict()
# create an instance of AiModelInsightsFiltersEcho from a dict
ai_model_insights_filters_echo_from_dict = AiModelInsightsFiltersEcho.from_dict(ai_model_insights_filters_echo_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


