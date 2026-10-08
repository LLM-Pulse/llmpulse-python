# CompetitorMentionsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[CompetitorMentionRecord]**](CompetitorMentionRecord.md) |  | 

## Example

```python
from llmpulse.models.competitor_mentions_response import CompetitorMentionsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorMentionsResponse from a JSON string
competitor_mentions_response_instance = CompetitorMentionsResponse.from_json(json)
# print the JSON string representation of the object
print(CompetitorMentionsResponse.to_json())

# convert the object into a dict
competitor_mentions_response_dict = competitor_mentions_response_instance.to_dict()
# create an instance of CompetitorMentionsResponse from a dict
competitor_mentions_response_from_dict = CompetitorMentionsResponse.from_dict(competitor_mentions_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


