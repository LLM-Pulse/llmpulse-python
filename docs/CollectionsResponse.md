# CollectionsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**collections** | [**List[TagRef]**](TagRef.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.collections_response import CollectionsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CollectionsResponse from a JSON string
collections_response_instance = CollectionsResponse.from_json(json)
# print the JSON string representation of the object
print(CollectionsResponse.to_json())

# convert the object into a dict
collections_response_dict = collections_response_instance.to_dict()
# create an instance of CollectionsResponse from a dict
collections_response_from_dict = CollectionsResponse.from_dict(collections_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


