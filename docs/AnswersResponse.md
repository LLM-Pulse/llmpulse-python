# AnswersResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[AnswerRecord]**](AnswerRecord.md) |  | 

## Example

```python
from llmpulse.models.answers_response import AnswersResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AnswersResponse from a JSON string
answers_response_instance = AnswersResponse.from_json(json)
# print the JSON string representation of the object
print(AnswersResponse.to_json())

# convert the object into a dict
answers_response_dict = answers_response_instance.to_dict()
# create an instance of AnswersResponse from a dict
answers_response_from_dict = AnswersResponse.from_dict(answers_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


