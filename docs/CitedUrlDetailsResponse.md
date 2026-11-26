# CitedUrlDetailsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**url_sha256** | **str** |  | 
**url** | **str** | The URL as first cited | 
**normalized_url** | **str** |  | 
**domain** | **str** |  | 
**host** | **str** |  | 
**stats** | [**CitedUrlDetailsResponseStats**](CitedUrlDetailsResponseStats.md) |  | 
**urls** | **List[Optional[str]]** | Up to 20 spellings of the URL as cited, alphabetically | 
**page_details** | [**CitationPageDetails**](CitationPageDetails.md) |  | 
**citation_series** | [**CitationSeries**](CitationSeries.md) |  | [optional] 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.cited_url_details_response import CitedUrlDetailsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CitedUrlDetailsResponse from a JSON string
cited_url_details_response_instance = CitedUrlDetailsResponse.from_json(json)
# print the JSON string representation of the object
print(CitedUrlDetailsResponse.to_json())

# convert the object into a dict
cited_url_details_response_dict = cited_url_details_response_instance.to_dict()
# create an instance of CitedUrlDetailsResponse from a dict
cited_url_details_response_from_dict = CitedUrlDetailsResponse.from_dict(cited_url_details_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


