# LocalBusinessesTotals


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**businesses** | **int** |  | [optional] 
**your_businesses** | **int** |  | [optional] 
**appearances** | **int** |  | [optional] 
**avg_rating** | **float** |  | [optional] 
**executions_with_local_businesses** | **int** |  | [optional] 

## Example

```python
from llmpulse.models.local_businesses_totals import LocalBusinessesTotals

# TODO update the JSON string below
json = "{}"
# create an instance of LocalBusinessesTotals from a JSON string
local_businesses_totals_instance = LocalBusinessesTotals.from_json(json)
# print the JSON string representation of the object
print(LocalBusinessesTotals.to_json())

# convert the object into a dict
local_businesses_totals_dict = local_businesses_totals_instance.to_dict()
# create an instance of LocalBusinessesTotals from a dict
local_businesses_totals_from_dict = LocalBusinessesTotals.from_dict(local_businesses_totals_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


