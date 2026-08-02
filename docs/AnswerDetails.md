# AnswerDetails


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**prompt_id** | **int** |  | [optional] 
**prompt_text** | **str** |  | [optional] 
**model** | **str** |  | [optional] 
**response** | **str** |  | [optional] 
**response_truncated** | **bool** |  | [optional] 
**executed_at** | **datetime** |  | [optional] 
**duration_ms** | **int** |  | [optional] 
**success** | **bool** |  | [optional] 
**fan_out_queries** | **List[str]** |  | [optional] 
**mentions** | **List[object]** |  | [optional] 
**citations** | **List[object]** |  | [optional] 
**competitor_mentions** | **List[object]** |  | [optional] 
**competitor_citations** | **List[object]** |  | [optional] 
**sentiments** | **List[object]** |  | [optional] 
**sources** | **List[object]** |  | [optional] 
**shopping_products** | **List[object]** |  | [optional] 
**brand_entities** | **List[object]** |  | [optional] 
**local_businesses** | **List[object]** |  | [optional] 
**locale** | [**AnswerDetailsLocale**](AnswerDetailsLocale.md) |  | [optional] 

## Example

```python
from llmpulse.models.answer_details import AnswerDetails

# TODO update the JSON string below
json = "{}"
# create an instance of AnswerDetails from a JSON string
answer_details_instance = AnswerDetails.from_json(json)
# print the JSON string representation of the object
print(AnswerDetails.to_json())

# convert the object into a dict
answer_details_dict = answer_details_instance.to_dict()
# create an instance of AnswerDetails from a dict
answer_details_from_dict = AnswerDetails.from_dict(answer_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


