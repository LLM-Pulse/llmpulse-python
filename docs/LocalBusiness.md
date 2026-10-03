# LocalBusiness


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**business_key** | **str** | Stable grouping key: the lowercased name and address | [optional] 
**title** | **str** |  | [optional] 
**address** | **str** |  | [optional] 
**domain** | **str** |  | [optional] 
**url** | **str** |  | [optional] 
**phone** | **str** |  | [optional] 
**avg_rating** | **float** |  | [optional] 
**reviews** | **int** |  | [optional] 
**avg_position** | **float** | Average rank of the business in the answer&#39;s list (1 &#x3D; first) | [optional] 
**prompts** | **int** |  | [optional] 
**appearances** | **int** |  | [optional] 
**is_client** | **bool** |  | [optional] 
**competitor_id** | **int** |  | [optional] 
**competitor_name** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.local_business import LocalBusiness

# TODO update the JSON string below
json = "{}"
# create an instance of LocalBusiness from a JSON string
local_business_instance = LocalBusiness.from_json(json)
# print the JSON string representation of the object
print(LocalBusiness.to_json())

# convert the object into a dict
local_business_dict = local_business_instance.to_dict()
# create an instance of LocalBusiness from a dict
local_business_from_dict = LocalBusiness.from_dict(local_business_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


