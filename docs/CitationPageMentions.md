# CitationPageMentions

The brands the cited page mentions, from its analysis for the requesting project. A page not yet analyzed for it has null brand_mentioned, competitor_mentioned and brand_position and empty lists.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**brand_mentioned** | **bool** |  | 
**competitor_mentioned** | **bool** |  | 
**brand_position** | **int** | Rank of the brand&#39;s first mention on the page; null when it has none | 
**content_gap_status** | **str** | missing_page_cache, content_unavailable, mentions_not_processed, mentioned, gap (a competitor but not the brand) or not_mentioned | 
**brands** | [**List[CitationPageMentionsBrandsInner]**](CitationPageMentionsBrandsInner.md) | Each brand the page mentions once, in order of first mention | 
**mentions** | [**List[CitationPageMentionsMentionsInner]**](CitationPageMentionsMentionsInner.md) | Every mention on the page with its snippet; not sent on GET /citation_intelligence/groups | [optional] 

## Example

```python
from llmpulse.models.citation_page_mentions import CitationPageMentions

# TODO update the JSON string below
json = "{}"
# create an instance of CitationPageMentions from a JSON string
citation_page_mentions_instance = CitationPageMentions.from_json(json)
# print the JSON string representation of the object
print(CitationPageMentions.to_json())

# convert the object into a dict
citation_page_mentions_dict = citation_page_mentions_instance.to_dict()
# create an instance of CitationPageMentions from a dict
citation_page_mentions_from_dict = CitationPageMentions.from_dict(citation_page_mentions_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


