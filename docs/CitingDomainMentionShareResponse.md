# CitingDomainMentionShareResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**filters** | [**CitationIntelligenceFiltersEcho**](CitationIntelligenceFiltersEcho.md) |  | 
**normalization** | **str** | How the shares are computed | 
**data** | [**List[CitingDomainMentionShareResponseDataInner]**](CitingDomainMentionShareResponseDataInner.md) | One row per requested domain (normalized, at most 50), in the order given | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.citing_domain_mention_share_response import CitingDomainMentionShareResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CitingDomainMentionShareResponse from a JSON string
citing_domain_mention_share_response_instance = CitingDomainMentionShareResponse.from_json(json)
# print the JSON string representation of the object
print(CitingDomainMentionShareResponse.to_json())

# convert the object into a dict
citing_domain_mention_share_response_dict = citing_domain_mention_share_response_instance.to_dict()
# create an instance of CitingDomainMentionShareResponse from a dict
citing_domain_mention_share_response_from_dict = CitingDomainMentionShareResponse.from_dict(citing_domain_mention_share_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


