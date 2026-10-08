# PaginatedEnvelope

Envelope shared by the paginated listings; each listing adds its own data rows

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.paginated_envelope import PaginatedEnvelope

# TODO update the JSON string below
json = "{}"
# create an instance of PaginatedEnvelope from a JSON string
paginated_envelope_instance = PaginatedEnvelope.from_json(json)
# print the JSON string representation of the object
print(PaginatedEnvelope.to_json())

# convert the object into a dict
paginated_envelope_dict = paginated_envelope_instance.to_dict()
# create an instance of PaginatedEnvelope from a dict
paginated_envelope_from_dict = PaginatedEnvelope.from_dict(paginated_envelope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


