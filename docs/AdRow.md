# AdRow

One row of /dimensions/ads. Fields depend on view: advertisers (domain, ads, executions, prompts, avg_position, best_position) and ads (id, model, title, snippet, url, domain, position, is_client, prompt_id, prompt_text, prompt_execution_id, executed_at).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **str** | Advertising domain; null on a placement that names none (view&#x3D;ads) | 
**ads** | **int** | Placements of the domain (view&#x3D;advertisers) | [optional] 
**executions** | **int** | Answers that carried them (view&#x3D;advertisers) | [optional] 
**prompts** | **int** | Distinct prompts that triggered them (view&#x3D;advertisers) | [optional] 
**avg_position** | **float** | Average position, 1 is the best slot; null when no placement has one (view&#x3D;advertisers) | [optional] 
**best_position** | **int** | Best position, 1 is the best slot (view&#x3D;advertisers) | [optional] 
**id** | **int** | The placement (view&#x3D;ads) | [optional] 
**model** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**snippet** | **str** |  | [optional] 
**url** | **str** |  | [optional] 
**position** | **int** | Position of the placement, 1 is the best slot (view&#x3D;ads) | [optional] 
**is_client** | **bool** | Whether the placement is identified as your brand&#39;s own (view&#x3D;ads) | [optional] 
**prompt_id** | **int** |  | [optional] 
**prompt_text** | **str** |  | [optional] 
**prompt_execution_id** | **int** |  | [optional] 
**executed_at** | **datetime** | When the answer that carried the placement was collected (view&#x3D;ads) | [optional] 

## Example

```python
from llmpulse.models.ad_row import AdRow

# TODO update the JSON string below
json = "{}"
# create an instance of AdRow from a JSON string
ad_row_instance = AdRow.from_json(json)
# print the JSON string representation of the object
print(AdRow.to_json())

# convert the object into a dict
ad_row_dict = ad_row_instance.to_dict()
# create an instance of AdRow from a dict
ad_row_from_dict = AdRow.from_dict(ad_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


