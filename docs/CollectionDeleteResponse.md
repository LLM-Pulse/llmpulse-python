# CollectionDeleteResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**deleted** | **bool** | Always true | 
**id** | **int** |  | 
**name** | **str** |  | 
**prompts_kept** | **int** | Prompts the collection held; they stay in the project | 
**total_collections** | **int** | Collections left in the project | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.collection_delete_response import CollectionDeleteResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CollectionDeleteResponse from a JSON string
collection_delete_response_instance = CollectionDeleteResponse.from_json(json)
# print the JSON string representation of the object
print(CollectionDeleteResponse.to_json())

# convert the object into a dict
collection_delete_response_dict = collection_delete_response_instance.to_dict()
# create an instance of CollectionDeleteResponse from a dict
collection_delete_response_from_dict = CollectionDeleteResponse.from_dict(collection_delete_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


