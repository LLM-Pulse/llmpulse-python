# MentionsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[MentionRecord]**](MentionRecord.md) |  | 

## Example

```python
from llmpulse.models.mentions_response import MentionsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of MentionsResponse from a JSON string
mentions_response_instance = MentionsResponse.from_json(json)
# print the JSON string representation of the object
print(MentionsResponse.to_json())

# convert the object into a dict
mentions_response_dict = mentions_response_instance.to_dict()
# create an instance of MentionsResponse from a dict
mentions_response_from_dict = MentionsResponse.from_dict(mentions_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


