# CitedUrlContentResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**url_sha256** | **str** |  | 
**url** | **str** | The URL as first cited | 
**normalized_url** | **str** |  | 
**domain** | **str** |  | 
**host** | **str** |  | 
**page_details** | [**CitationPageDetails**](CitationPageDetails.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.cited_url_content_response import CitedUrlContentResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CitedUrlContentResponse from a JSON string
cited_url_content_response_instance = CitedUrlContentResponse.from_json(json)
# print the JSON string representation of the object
print(CitedUrlContentResponse.to_json())

# convert the object into a dict
cited_url_content_response_dict = cited_url_content_response_instance.to_dict()
# create an instance of CitedUrlContentResponse from a dict
cited_url_content_response_from_dict = CitedUrlContentResponse.from_dict(cited_url_content_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


