# OwnedMediaCitingAnswer


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**answer_id** | **int** | The answer (prompt execution) id, readable with GET /answers/{id} | [optional] 
**prompt_id** | **int** |  | [optional] 
**prompt_text** | **str** |  | [optional] 
**model** | **str** |  | [optional] 
**country_code** | **str** |  | [optional] 
**language_code** | **str** |  | [optional] 
**executed_at** | **datetime** |  | [optional] 
**excerpt** | **str** | The start of the answer as plain text (at most 300 characters) | [optional] 
**app_url** | **str** | The answer in the app | [optional] 

## Example

```python
from llmpulse.models.owned_media_citing_answer import OwnedMediaCitingAnswer

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaCitingAnswer from a JSON string
owned_media_citing_answer_instance = OwnedMediaCitingAnswer.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaCitingAnswer.to_json())

# convert the object into a dict
owned_media_citing_answer_dict = owned_media_citing_answer_instance.to_dict()
# create an instance of OwnedMediaCitingAnswer from a dict
owned_media_citing_answer_from_dict = OwnedMediaCitingAnswer.from_dict(owned_media_citing_answer_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


