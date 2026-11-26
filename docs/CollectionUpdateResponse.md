# CollectionUpdateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**collection** | [**CollectionUpdateResponseCollection**](CollectionUpdateResponseCollection.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.collection_update_response import CollectionUpdateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CollectionUpdateResponse from a JSON string
collection_update_response_instance = CollectionUpdateResponse.from_json(json)
# print the JSON string representation of the object
print(CollectionUpdateResponse.to_json())

# convert the object into a dict
collection_update_response_dict = collection_update_response_instance.to_dict()
# create an instance of CollectionUpdateResponse from a dict
collection_update_response_from_dict = CollectionUpdateResponse.from_dict(collection_update_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


