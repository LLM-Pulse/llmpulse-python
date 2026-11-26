# CitationPageMentionsBrandsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actor_type** | **str** | project or competitor | 
**competitor_id** | **int** | Null for the project | 
**name** | **str** |  | 
**domain** | **str** | The competitor&#39;s domain, or the project&#39;s URL (null when it has none) | 
**position** | **int** |  | 

## Example

```python
from llmpulse.models.citation_page_mentions_brands_inner import CitationPageMentionsBrandsInner

# TODO update the JSON string below
json = "{}"
# create an instance of CitationPageMentionsBrandsInner from a JSON string
citation_page_mentions_brands_inner_instance = CitationPageMentionsBrandsInner.from_json(json)
# print the JSON string representation of the object
print(CitationPageMentionsBrandsInner.to_json())

# convert the object into a dict
citation_page_mentions_brands_inner_dict = citation_page_mentions_brands_inner_instance.to_dict()
# create an instance of CitationPageMentionsBrandsInner from a dict
citation_page_mentions_brands_inner_from_dict = CitationPageMentionsBrandsInner.from_dict(citation_page_mentions_brands_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


