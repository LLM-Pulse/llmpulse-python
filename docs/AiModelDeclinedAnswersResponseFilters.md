# AiModelDeclinedAnswersResponseFilters

The prompt filters the counts were computed with, as the server resolved them. A filter that was not given is left out; model is always there.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model** | **str** |  | [optional] 
**country_code** | **str** | Comma-separated country codes | [optional] 
**language_code** | **str** | Comma-separated language codes | [optional] 
**collection_id** | **str** | Comma-separated collection ids | [optional] 
**prompt_type** | **str** | Comma-separated prompt types | [optional] 
**brand_kind** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.ai_model_declined_answers_response_filters import AiModelDeclinedAnswersResponseFilters

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelDeclinedAnswersResponseFilters from a JSON string
ai_model_declined_answers_response_filters_instance = AiModelDeclinedAnswersResponseFilters.from_json(json)
# print the JSON string representation of the object
print(AiModelDeclinedAnswersResponseFilters.to_json())

# convert the object into a dict
ai_model_declined_answers_response_filters_dict = ai_model_declined_answers_response_filters_instance.to_dict()
# create an instance of AiModelDeclinedAnswersResponseFilters from a dict
ai_model_declined_answers_response_filters_from_dict = AiModelDeclinedAnswersResponseFilters.from_dict(ai_model_declined_answers_response_filters_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


