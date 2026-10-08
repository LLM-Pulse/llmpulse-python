# CollectionCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**collection** | [**CollectionCreateResponseCollection**](CollectionCreateResponseCollection.md) |  | 
**prompts_attached** | **int** | Existing prompts attached through prompt_ids | 
**total_collections** | **int** |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.collection_create_response import CollectionCreateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CollectionCreateResponse from a JSON string
collection_create_response_instance = CollectionCreateResponse.from_json(json)
# print the JSON string representation of the object
print(CollectionCreateResponse.to_json())

# convert the object into a dict
collection_create_response_dict = collection_create_response_instance.to_dict()
# create an instance of CollectionCreateResponse from a dict
collection_create_response_from_dict = CollectionCreateResponse.from_dict(collection_create_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


