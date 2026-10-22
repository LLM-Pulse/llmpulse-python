# ProjectDetailsAllOfSearchConsole

Google Search Console connection of the project, judged by its primary property. connected means the Search Console endpoints can answer; reconnect_required means Google refused the primary property's stored access, so reads without property return ERR_SEARCH_CONSOLE_ACCESS_REVOKED until it is reconnected at connect_url, while a property GET /search_console/properties lists as connected, or property=all, still answers; not_connected means the endpoints return ERR_SEARCH_CONSOLE_NOT_CONNECTED.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**var_property** | **str** | The primary property (e.g. sc-domain:example.com), null when not connected | [optional] 
**connect_url** | **str** | The in-app page where the property is connected or reconnected (Preferences &gt; Project Settings &gt; Data Connections) | [optional] 
**properties_count** | **int** | Connected properties Google still accepts (reconnect_required ones excluded); GET /search_console/properties lists every property with its status | [optional] 

## Example

```python
from llmpulse.models.project_details_all_of_search_console import ProjectDetailsAllOfSearchConsole

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDetailsAllOfSearchConsole from a JSON string
project_details_all_of_search_console_instance = ProjectDetailsAllOfSearchConsole.from_json(json)
# print the JSON string representation of the object
print(ProjectDetailsAllOfSearchConsole.to_json())

# convert the object into a dict
project_details_all_of_search_console_dict = project_details_all_of_search_console_instance.to_dict()
# create an instance of ProjectDetailsAllOfSearchConsole from a dict
project_details_all_of_search_console_from_dict = ProjectDetailsAllOfSearchConsole.from_dict(project_details_all_of_search_console_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


