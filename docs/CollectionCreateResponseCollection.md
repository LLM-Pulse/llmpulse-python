# CollectionCreateResponseCollection


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 
**description** | **str** |  | 

## Example

```python
from llmpulse.models.collection_create_response_collection import CollectionCreateResponseCollection

# TODO update the JSON string below
json = "{}"
# create an instance of CollectionCreateResponseCollection from a JSON string
collection_create_response_collection_instance = CollectionCreateResponseCollection.from_json(json)
# print the JSON string representation of the object
print(CollectionCreateResponseCollection.to_json())

# convert the object into a dict
collection_create_response_collection_dict = collection_create_response_collection_instance.to_dict()
# create an instance of CollectionCreateResponseCollection from a dict
collection_create_response_collection_from_dict = CollectionCreateResponseCollection.from_dict(collection_create_response_collection_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


