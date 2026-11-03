# AiModelCitationsRow


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model** | **str** | AI model key, as /dimensions/models lists it | [optional] 
**label** | **str** | Display name of the model | [optional] 
**color** | **str** | Hex color the app charts the model with | [optional] 
**citations_count** | **int** | Citations of the brand&#39;s URLs in the model&#39;s answers; 0 when it has none | [optional] 
**share_of_total** | **float** | The model&#39;s percentage (0-100) of total_citations; null when total_citations is 0 | [optional] 

## Example

```python
from llmpulse.models.ai_model_citations_row import AiModelCitationsRow

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelCitationsRow from a JSON string
ai_model_citations_row_instance = AiModelCitationsRow.from_json(json)
# print the JSON string representation of the object
print(AiModelCitationsRow.to_json())

# convert the object into a dict
ai_model_citations_row_dict = ai_model_citations_row_instance.to_dict()
# create an instance of AiModelCitationsRow from a dict
ai_model_citations_row_from_dict = AiModelCitationsRow.from_dict(ai_model_citations_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


