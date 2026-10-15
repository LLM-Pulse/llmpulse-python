# OwnedMediaStoreTotals


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**store** | **str** |  | [optional] 
**total** | **int** |  | [optional] 
**yours** | **int** |  | [optional] 
**share_pct** | **float** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_store_totals import OwnedMediaStoreTotals

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaStoreTotals from a JSON string
owned_media_store_totals_instance = OwnedMediaStoreTotals.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaStoreTotals.to_json())

# convert the object into a dict
owned_media_store_totals_dict = owned_media_store_totals_instance.to_dict()
# create an instance of OwnedMediaStoreTotals from a dict
owned_media_store_totals_from_dict = OwnedMediaStoreTotals.from_dict(owned_media_store_totals_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


