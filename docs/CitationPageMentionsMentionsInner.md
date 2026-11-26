# CitationPageMentionsMentionsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**matched_key** | **str** | The name that matched | 
**snippet** | **str** |  | 
**start_offset** | **int** |  | 
**end_offset** | **int** |  | 
**position** | **int** |  | 
**actor_type** | **str** | project or competitor | 
**competitor_id** | **int** | Null for the project | 
**actor_name** | **str** |  | 
**actor_domain** | **str** | The competitor&#39;s domain, or the project&#39;s URL | 

## Example

```python
from llmpulse.models.citation_page_mentions_mentions_inner import CitationPageMentionsMentionsInner

# TODO update the JSON string below
json = "{}"
# create an instance of CitationPageMentionsMentionsInner from a JSON string
citation_page_mentions_mentions_inner_instance = CitationPageMentionsMentionsInner.from_json(json)
# print the JSON string representation of the object
print(CitationPageMentionsMentionsInner.to_json())

# convert the object into a dict
citation_page_mentions_mentions_inner_dict = citation_page_mentions_mentions_inner_instance.to_dict()
# create an instance of CitationPageMentionsMentionsInner from a dict
citation_page_mentions_mentions_inner_from_dict = CitationPageMentionsMentionsInner.from_dict(citation_page_mentions_mentions_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


