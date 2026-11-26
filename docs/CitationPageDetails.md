# CitationPageDetails


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url_sha256** | **str** |  | 
**normalized_url** | **str** |  | 
**page_cache** | [**CitationPageCache**](CitationPageCache.md) |  | 
**page_mentions** | [**CitationPageMentions**](CitationPageMentions.md) |  | 
**content** | [**CitationPageDetailsContent**](CitationPageDetailsContent.md) |  | [optional] 

## Example

```python
from llmpulse.models.citation_page_details import CitationPageDetails

# TODO update the JSON string below
json = "{}"
# create an instance of CitationPageDetails from a JSON string
citation_page_details_instance = CitationPageDetails.from_json(json)
# print the JSON string representation of the object
print(CitationPageDetails.to_json())

# convert the object into a dict
citation_page_details_dict = citation_page_details_instance.to_dict()
# create an instance of CitationPageDetails from a dict
citation_page_details_from_dict = CitationPageDetails.from_dict(citation_page_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


