# CitedUrlOccurrencesResponseAllOfData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source_id** | **int** |  | 
**answer_id** | **int** |  | 
**prompt_execution_id** | **int** | Same as answer_id | 
**prompt_id** | **int** |  | 
**prompt_text** | **str** |  | 
**model** | **str** |  | 
**executed_at** | **datetime** |  | 
**citation_position** | **int** | Rank of the citation in the answer; 0 for a background source reference | 
**url** | **str** | Normalized cited URL | 
**domain** | **str** |  | 
**source_type** | **str** | owned, competitor or third_party | 
**response_excerpt** | **str** | The first 600 characters of the answer | 
**response_truncated** | **bool** |  | 
**fan_out_queries** | **List[str]** | Sub-queries the model issued while answering; null when the model reports none | 

## Example

```python
from llmpulse.models.cited_url_occurrences_response_all_of_data import CitedUrlOccurrencesResponseAllOfData

# TODO update the JSON string below
json = "{}"
# create an instance of CitedUrlOccurrencesResponseAllOfData from a JSON string
cited_url_occurrences_response_all_of_data_instance = CitedUrlOccurrencesResponseAllOfData.from_json(json)
# print the JSON string representation of the object
print(CitedUrlOccurrencesResponseAllOfData.to_json())

# convert the object into a dict
cited_url_occurrences_response_all_of_data_dict = cited_url_occurrences_response_all_of_data_instance.to_dict()
# create an instance of CitedUrlOccurrencesResponseAllOfData from a dict
cited_url_occurrences_response_all_of_data_from_dict = CitedUrlOccurrencesResponseAllOfData.from_dict(cited_url_occurrences_response_all_of_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


