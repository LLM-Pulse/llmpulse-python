# SentimentsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[SentimentRecord]**](SentimentRecord.md) |  | 

## Example

```python
from llmpulse.models.sentiments_response import SentimentsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SentimentsResponse from a JSON string
sentiments_response_instance = SentimentsResponse.from_json(json)
# print the JSON string representation of the object
print(SentimentsResponse.to_json())

# convert the object into a dict
sentiments_response_dict = sentiments_response_instance.to_dict()
# create an instance of SentimentsResponse from a dict
sentiments_response_from_dict = SentimentsResponse.from_dict(sentiments_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


