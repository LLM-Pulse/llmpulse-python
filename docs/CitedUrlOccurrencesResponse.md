# CitedUrlOccurrencesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**url_sha256** | **str** |  | 
**data** | [**List[CitedUrlOccurrencesResponseAllOfData]**](CitedUrlOccurrencesResponseAllOfData.md) | One row per citation of the URL, latest answer first | 

## Example

```python
from llmpulse.models.cited_url_occurrences_response import CitedUrlOccurrencesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CitedUrlOccurrencesResponse from a JSON string
cited_url_occurrences_response_instance = CitedUrlOccurrencesResponse.from_json(json)
# print the JSON string representation of the object
print(CitedUrlOccurrencesResponse.to_json())

# convert the object into a dict
cited_url_occurrences_response_dict = cited_url_occurrences_response_instance.to_dict()
# create an instance of CitedUrlOccurrencesResponse from a dict
cited_url_occurrences_response_from_dict = CitedUrlOccurrencesResponse.from_dict(cited_url_occurrences_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


