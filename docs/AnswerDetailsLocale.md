# AnswerDetailsLocale


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country_code** | **str** |  | [optional] 
**language_code** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.answer_details_locale import AnswerDetailsLocale

# TODO update the JSON string below
json = "{}"
# create an instance of AnswerDetailsLocale from a JSON string
answer_details_locale_instance = AnswerDetailsLocale.from_json(json)
# print the JSON string representation of the object
print(AnswerDetailsLocale.to_json())

# convert the object into a dict
answer_details_locale_dict = answer_details_locale_instance.to_dict()
# create an instance of AnswerDetailsLocale from a dict
answer_details_locale_from_dict = AnswerDetailsLocale.from_dict(answer_details_locale_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


