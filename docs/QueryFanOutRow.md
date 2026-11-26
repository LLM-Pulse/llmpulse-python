# QueryFanOutRow

A view=query row carries query_text, count and share; a view=prompt row carries prompt_id, prompt_text, variations_count and total_count

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query_text** | **str** | The sub-query a model issued (view&#x3D;query) | [optional] 
**count** | **int** | Times it was issued (view&#x3D;query) | [optional] 
**share** | **float** | Share of all sub-query occurrences, on a 0-100 scale (view&#x3D;query) | [optional] 
**prompt_id** | **int** | view&#x3D;prompt | [optional] 
**prompt_text** | **str** | view&#x3D;prompt | [optional] 
**variations_count** | **int** | Distinct sub-queries issued for the prompt (view&#x3D;prompt) | [optional] 
**total_count** | **int** | Sub-queries issued for the prompt, repeats included (view&#x3D;prompt) | [optional] 

## Example

```python
from llmpulse.models.query_fan_out_row import QueryFanOutRow

# TODO update the JSON string below
json = "{}"
# create an instance of QueryFanOutRow from a JSON string
query_fan_out_row_instance = QueryFanOutRow.from_json(json)
# print the JSON string representation of the object
print(QueryFanOutRow.to_json())

# convert the object into a dict
query_fan_out_row_dict = query_fan_out_row_instance.to_dict()
# create an instance of QueryFanOutRow from a dict
query_fan_out_row_from_dict = QueryFanOutRow.from_dict(query_fan_out_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


