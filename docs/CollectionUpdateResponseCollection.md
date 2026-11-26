# CollectionUpdateResponseCollection


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 
**description** | **str** |  | 
**prompts_count** | **int** |  | 

## Example

```python
from llmpulse.models.collection_update_response_collection import CollectionUpdateResponseCollection

# TODO update the JSON string below
json = "{}"
# create an instance of CollectionUpdateResponseCollection from a JSON string
collection_update_response_collection_instance = CollectionUpdateResponseCollection.from_json(json)
# print the JSON string representation of the object
print(CollectionUpdateResponseCollection.to_json())

# convert the object into a dict
collection_update_response_collection_dict = collection_update_response_collection_instance.to_dict()
# create an instance of CollectionUpdateResponseCollection from a dict
collection_update_response_collection_from_dict = CollectionUpdateResponseCollection.from_dict(collection_update_response_collection_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


