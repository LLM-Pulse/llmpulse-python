# ProjectDetailsAllOfBingWebmaster

Bing Webmaster Tools site behind /bing_webmaster. connected means its endpoints answer; reconnect_required means Bing refused the stored API key or the site is no longer verified, so the endpoints still answer from the data already synced, which stops updating until the site is reconnected at connect_url; not_connected means they return ERR_BING_WEBMASTER_NOT_CONNECTED.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**site** | **str** | The connected site (e.g. https://example.com/), null when not connected | [optional] 
**last_synced_at** | **datetime** | When that site last synced, null before its first sync | [optional] 
**connect_url** | **str** | The in-app page where the site is connected or reconnected (Preferences &gt; Project Settings &gt; Connections) | [optional] 

## Example

```python
from llmpulse.models.project_details_all_of_bing_webmaster import ProjectDetailsAllOfBingWebmaster

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDetailsAllOfBingWebmaster from a JSON string
project_details_all_of_bing_webmaster_instance = ProjectDetailsAllOfBingWebmaster.from_json(json)
# print the JSON string representation of the object
print(ProjectDetailsAllOfBingWebmaster.to_json())

# convert the object into a dict
project_details_all_of_bing_webmaster_dict = project_details_all_of_bing_webmaster_instance.to_dict()
# create an instance of ProjectDetailsAllOfBingWebmaster from a dict
project_details_all_of_bing_webmaster_from_dict = ProjectDetailsAllOfBingWebmaster.from_dict(project_details_all_of_bing_webmaster_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


