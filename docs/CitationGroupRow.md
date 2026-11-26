# CitationGroupRow

A cited URL, domain or host (view). url-view rows carry url, url_sha256 and normalized_url, plus page_cache and page_mentions when page details are included; domain and host rows carry domain or host and aggregate_details.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source_id** | **int** | The group&#39;s first citation | 
**view** | **str** | url, domain or host | 
**key** | **str** | The URL as cited, the domain or the host | 
**total_responses** | **int** | Answers citing it | 
**total_citations** | **int** |  | 
**citation_rate** | **float** | total_responses as a percentage (0-100) of citation_rate_denominator | 
**citation_rate_denominator** | **int** | Answers matching the filters | 
**avg_citation_position** | **float** | Null when no visible citation has a rank | 
**first_seen_at** | **datetime** |  | 
**last_seen_at** | **datetime** |  | 
**models** | **Dict[str, int]** | Answers citing it per AI model, keyed by model | 
**url** | **str** | url view only. The URL as cited | [optional] 
**url_sha256** | **str** | url view only. Key of the cited page, shared by the URL&#39;s variants | [optional] 
**normalized_url** | **str** | url view only | [optional] 
**page_cache** | [**CitationPageCache**](CitationPageCache.md) |  | [optional] 
**page_mentions** | [**CitationPageMentions**](CitationPageMentions.md) |  | [optional] 
**domain** | **str** | domain view only | [optional] 
**host** | **str** | host view only | [optional] 
**aggregate_details** | [**CitationGroupRowAggregateDetails**](CitationGroupRowAggregateDetails.md) |  | [optional] 
**citation_series** | [**CitationSeries**](CitationSeries.md) |  | [optional] 

## Example

```python
from llmpulse.models.citation_group_row import CitationGroupRow

# TODO update the JSON string below
json = "{}"
# create an instance of CitationGroupRow from a JSON string
citation_group_row_instance = CitationGroupRow.from_json(json)
# print the JSON string representation of the object
print(CitationGroupRow.to_json())

# convert the object into a dict
citation_group_row_dict = citation_group_row_instance.to_dict()
# create an instance of CitationGroupRow from a dict
citation_group_row_from_dict = CitationGroupRow.from_dict(citation_group_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


