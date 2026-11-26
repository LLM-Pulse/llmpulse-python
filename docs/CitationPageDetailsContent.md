# CitationPageDetailsContent

GET /citation_intelligence/urls/{url_sha256}/content only. Both null when the page has no usable content.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | The page text | 
**rendered_html** | **str** | Sanitized HTML of the page | 

## Example

```python
from llmpulse.models.citation_page_details_content import CitationPageDetailsContent

# TODO update the JSON string below
json = "{}"
# create an instance of CitationPageDetailsContent from a JSON string
citation_page_details_content_instance = CitationPageDetailsContent.from_json(json)
# print the JSON string representation of the object
print(CitationPageDetailsContent.to_json())

# convert the object into a dict
citation_page_details_content_dict = citation_page_details_content_instance.to_dict()
# create an instance of CitationPageDetailsContent from a dict
citation_page_details_content_from_dict = CitationPageDetailsContent.from_dict(citation_page_details_content_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


