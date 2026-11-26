# AnalystScoreRow

One analyst model's score of one brand (a subject in a custom study) on one attribute of one dimension

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**brand** | **str** | Brand name; the subject name in a custom study | 
**is_project** | **bool** | Whether it is the project&#39;s own brand; in a custom study, the focus subject | 
**model** | **str** |  | 
**report_date** | **date** |  | 
**dimension** | **str** | Dimension key, as the dimension filter takes it | 
**dimension_name** | **str** |  | 
**attribute** | **str** | Attribute key within the dimension | 
**attribute_name** | **str** |  | 
**score** | **object** | The 0-100 score as the analyst model wrote it, normally a number, or null when it gave none. Deliberately untyped, as the model&#39;s output is stored without coercion | 
**reasoning** | **str** | Why the model gave this score; null when it gave no reasoning | 

## Example

```python
from llmpulse.models.analyst_score_row import AnalystScoreRow

# TODO update the JSON string below
json = "{}"
# create an instance of AnalystScoreRow from a JSON string
analyst_score_row_instance = AnalystScoreRow.from_json(json)
# print the JSON string representation of the object
print(AnalystScoreRow.to_json())

# convert the object into a dict
analyst_score_row_dict = analyst_score_row_instance.to_dict()
# create an instance of AnalystScoreRow from a dict
analyst_score_row_from_dict = AnalystScoreRow.from_dict(analyst_score_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


