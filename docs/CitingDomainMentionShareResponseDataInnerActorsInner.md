# CitingDomainMentionShareResponseDataInnerActorsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | brand or competitor | 
**id** | **int** | Null for the brand, the competitor id otherwise | 
**name** | **str** |  | 
**mentions** | **int** |  | 
**share** | **float** | mentions as a percentage (0-100) of total_mentions | 

## Example

```python
from llmpulse.models.citing_domain_mention_share_response_data_inner_actors_inner import CitingDomainMentionShareResponseDataInnerActorsInner

# TODO update the JSON string below
json = "{}"
# create an instance of CitingDomainMentionShareResponseDataInnerActorsInner from a JSON string
citing_domain_mention_share_response_data_inner_actors_inner_instance = CitingDomainMentionShareResponseDataInnerActorsInner.from_json(json)
# print the JSON string representation of the object
print(CitingDomainMentionShareResponseDataInnerActorsInner.to_json())

# convert the object into a dict
citing_domain_mention_share_response_data_inner_actors_inner_dict = citing_domain_mention_share_response_data_inner_actors_inner_instance.to_dict()
# create an instance of CitingDomainMentionShareResponseDataInnerActorsInner from a dict
citing_domain_mention_share_response_data_inner_actors_inner_from_dict = CitingDomainMentionShareResponseDataInnerActorsInner.from_dict(citing_domain_mention_share_response_data_inner_actors_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


