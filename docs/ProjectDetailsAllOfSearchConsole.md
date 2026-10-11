# ProjectDetailsAllOfSearchConsole

Google Search Console connection of the project. connected means the Search Console endpoints can answer; reconnect_required means Google refused the stored access and the property must be reconnected in Preferences > Project Settings > Data Connections.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**var_property** | **str** | The connected property (e.g. sc-domain:example.com), null when not connected | [optional] 

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


