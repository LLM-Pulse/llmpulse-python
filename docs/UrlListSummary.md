# UrlListSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**entries_count** | **int** |  | 
**cited_entries** | **int** |  | 
**citations** | **int** | AI answers citing any entry in the window, each once. | 
**answers** | **int** | AI answers in the window, the citation rate&#39;s denominator. | 
**citation_rate** | **float** | citations over answers, in percent. | 
**avg_citation_position** | **float** |  | 
**median_days_to_first_citation** | **int** |  | 
**total_cost** | **float** |  | 
**cost_per_cited_entry** | **float** |  | 

## Example

```python
from llmpulse.models.url_list_summary import UrlListSummary

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListSummary from a JSON string
url_list_summary_instance = UrlListSummary.from_json(json)
# print the JSON string representation of the object
print(UrlListSummary.to_json())

# convert the object into a dict
url_list_summary_dict = url_list_summary_instance.to_dict()
# create an instance of UrlListSummary from a dict
url_list_summary_from_dict = UrlListSummary.from_dict(url_list_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


