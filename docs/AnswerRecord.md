# AnswerRecord

One answer. Without query a row carries response and response_truncated; with query it carries snippet and match_count instead

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**prompt_id** | **int** |  | 
**prompt_text** | **str** |  | 
**model** | **str** |  | 
**executed_at** | **datetime** |  | 
**duration_ms** | **float** | Milliseconds our pipeline spent processing the collected answer, rounded to one decimal place | 
**no_result** | **bool** | True for a sentinel non-answer (no answer could be collected after all retries, or the model declined to answer, today only Gemini); excluded from platform metrics | 
**no_result_reason** | **str** | Present only when no_result is true. declined &#x3D; the model declined to answer and response holds its reply; no_answer &#x3D; no answer could be collected | [optional] 
**mentions_count** | **int** | Mentions of your brand in the answer | 
**citations_count** | **int** | Citations of your brand in the answer | 
**app_url** | **str** | Opens this answer in the app. The link names its project, so it opens there for any user with access to that project | 
**response** | **str** | The answer text, cut to 10,000 characters (without query) | [optional] 
**response_truncated** | **bool** | Whether response was cut (without query) | [optional] 
**snippet** | **str** | The text around the first match (with query) | [optional] 
**match_count** | **int** | Matches of query in the answer (with query) | [optional] 

## Example

```python
from llmpulse.models.answer_record import AnswerRecord

# TODO update the JSON string below
json = "{}"
# create an instance of AnswerRecord from a JSON string
answer_record_instance = AnswerRecord.from_json(json)
# print the JSON string representation of the object
print(AnswerRecord.to_json())

# convert the object into a dict
answer_record_dict = answer_record_instance.to_dict()
# create an instance of AnswerRecord from a dict
answer_record_from_dict = AnswerRecord.from_dict(answer_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


