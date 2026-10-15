# OwnedMediaSummaryResponsePrevious

The period of the same length that ends just before from

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_from** | **datetime** |  | [optional] 
**to** | **datetime** |  | [optional] 
**kpis** | [**OwnedMediaKpis**](OwnedMediaKpis.md) |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_summary_response_previous import OwnedMediaSummaryResponsePrevious

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaSummaryResponsePrevious from a JSON string
owned_media_summary_response_previous_instance = OwnedMediaSummaryResponsePrevious.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaSummaryResponsePrevious.to_json())

# convert the object into a dict
owned_media_summary_response_previous_dict = owned_media_summary_response_previous_instance.to_dict()
# create an instance of OwnedMediaSummaryResponsePrevious from a dict
owned_media_summary_response_previous_from_dict = OwnedMediaSummaryResponsePrevious.from_dict(owned_media_summary_response_previous_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


