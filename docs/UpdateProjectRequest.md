# UpdateProjectRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Project name shown in the app. A label: it does not change mention detection unless brand_name is empty. Cannot be blank | [optional] 
**brand_name** | **str** | Brand name used to detect mentions. Applies to future runs; it does not rewrite history | [optional] 
**description** | **str** | What the brand does. Context for Recommendations and GEO Writer (Brand Book) | [optional] 
**industry** | **str** | Single industry key (e.g. SAAS), stored as sent; an array of keys is also accepted and stored as an array, like the in-app multi-select. Unknown keys are rejected with the valid keys listed | [optional] 
**business_model** | **str** | Business model key (e.g. B2B_SAAS); unknown keys are rejected | [optional] 
**business_model_other** | **str** | Free-text business model, only accepted when business_model is OTHER; rejected against any other key | [optional] 
**target_audience** | **str** | Who the brand sells to (Brand Book) | [optional] 
**brand_voice** | **str** | Tone of voice guidance for generated content (Brand Book) | [optional] 
**goals** | **str** | What the brand wants to achieve. Context for GEO Writer and prompt suggestions | [optional] 
**primary_products** | **List[str]** | Full replacement list of the main products or services | [optional] 
**matching_names** | **List[str]** | FULL replacement list of the brand-name variants used to detect mentions; send every variant to keep | [optional] 
**additional_owned_domains** | **List[str]** | FULL replacement list (at most 10) of other domains the brand owns, such as a blog or a country site; [] clears it. Citations from them count as owned, like the project website. Each entry is a website&#39;s own domain and covers its subdomains; a pasted URL is stored as its domain (https://www.acme.co.uk/x becomes acme.co.uk). A list the domain editor would refuse (a subdomain such as blog.acme.com, a platform many companies share such as youtube.com, amazon.com or wordpress.com, the project website, a tracked competitor domain, a duplicate or an entry that is not a domain) is rejected with ERR_INVALID_PARAM and the reason. Order does not matter, and an unchanged list starts nothing. Account owner only, on every plan | [optional] 

## Example

```python
from llmpulse.models.update_project_request import UpdateProjectRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateProjectRequest from a JSON string
update_project_request_instance = UpdateProjectRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateProjectRequest.to_json())

# convert the object into a dict
update_project_request_dict = update_project_request_instance.to_dict()
# create an instance of UpdateProjectRequest from a dict
update_project_request_from_dict = UpdateProjectRequest.from_dict(update_project_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


