# CitationGroupRowAggregateDetails

domain and host views only. The distinct cited pages of the group.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**unique_urls_count** | **int** |  | 
**crawled_urls_count** | **int** | Pages with usable content | 
**brand_mentioned_urls_count** | **int** | Pages analyzed for the project that mention the brand; null when none is analyzed | 
**competitor_mentioned_urls_count** | **int** | Pages analyzed for the project that mention a competitor; null when none is analyzed | 
**last_crawled_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.citation_group_row_aggregate_details import CitationGroupRowAggregateDetails

# TODO update the JSON string below
json = "{}"
# create an instance of CitationGroupRowAggregateDetails from a JSON string
citation_group_row_aggregate_details_instance = CitationGroupRowAggregateDetails.from_json(json)
# print the JSON string representation of the object
print(CitationGroupRowAggregateDetails.to_json())

# convert the object into a dict
citation_group_row_aggregate_details_dict = citation_group_row_aggregate_details_instance.to_dict()
# create an instance of CitationGroupRowAggregateDetails from a dict
citation_group_row_aggregate_details_from_dict = CitationGroupRowAggregateDetails.from_dict(citation_group_row_aggregate_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


