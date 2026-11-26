# CitationPageCache

What was read on the cited page. Metadata is null when the page has no usable content.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**present** | **bool** | Whether the page has a saved copy | 
**last_crawled_at** | **datetime** | When the saved copy was read; null without usable content | 
**status_code** | **int** | A saved successful response or an observed 404/410; null otherwise | 
**error_message** | **str** | Always null; crawl errors are not exposed | 
**content_format** | **str** |  | 
**bytes** | **int** |  | 
**html_title** | **str** |  | 
**meta_title** | **str** |  | 
**meta_description** | **str** |  | 
**h1** | **str** |  | 
**canonical_url** | **str** |  | 
**language** | **str** |  | 
**mentions_processed** | **bool** | Whether the page&#39;s mention analysis has completed for this project | 
**content_available** | **bool** |  | 

## Example

```python
from llmpulse.models.citation_page_cache import CitationPageCache

# TODO update the JSON string below
json = "{}"
# create an instance of CitationPageCache from a JSON string
citation_page_cache_instance = CitationPageCache.from_json(json)
# print the JSON string representation of the object
print(CitationPageCache.to_json())

# convert the object into a dict
citation_page_cache_dict = citation_page_cache_instance.to_dict()
# create an instance of CitationPageCache from a dict
citation_page_cache_from_dict = CitationPageCache.from_dict(citation_page_cache_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


