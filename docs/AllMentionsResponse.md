# AllMentionsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[AllMentionRecord]**](AllMentionRecord.md) |  | 

## Example

```python
from llmpulse.models.all_mentions_response import AllMentionsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AllMentionsResponse from a JSON string
all_mentions_response_instance = AllMentionsResponse.from_json(json)
# print the JSON string representation of the object
print(AllMentionsResponse.to_json())

# convert the object into a dict
all_mentions_response_dict = all_mentions_response_instance.to_dict()
# create an instance of AllMentionsResponse from a dict
all_mentions_response_from_dict = AllMentionsResponse.from_dict(all_mentions_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


