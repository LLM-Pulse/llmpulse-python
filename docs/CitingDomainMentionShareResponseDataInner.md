# CitingDomainMentionShareResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **str** |  | 
**responses_citing** | **int** | Answers citing the domain | 
**total_mentions** | **int** | Brand and competitor mentions in those answers, each answer counted once per brand | 
**actors** | [**List[CitingDomainMentionShareResponseDataInnerActorsInner]**](CitingDomainMentionShareResponseDataInnerActorsInner.md) | The brand and every competitor, most mentions first; empty when no answer cites the domain | 

## Example

```python
from llmpulse.models.citing_domain_mention_share_response_data_inner import CitingDomainMentionShareResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of CitingDomainMentionShareResponseDataInner from a JSON string
citing_domain_mention_share_response_data_inner_instance = CitingDomainMentionShareResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(CitingDomainMentionShareResponseDataInner.to_json())

# convert the object into a dict
citing_domain_mention_share_response_data_inner_dict = citing_domain_mention_share_response_data_inner_instance.to_dict()
# create an instance of CitingDomainMentionShareResponseDataInner from a dict
citing_domain_mention_share_response_data_inner_from_dict = CitingDomainMentionShareResponseDataInner.from_dict(citing_domain_mention_share_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


