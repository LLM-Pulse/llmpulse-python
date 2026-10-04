# llmpulse.AccountApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_account**](AccountApi.md#get_account) | **GET** /account | Account plan, quota usage and rate limits


# **get_account**
> GetAccount200Response get_account()

Account plan, quota usage and rate limits

Returns the account plan, tracking cadence, subscription window, how much of each quota is used (prompts, projects, competitors per project, monthly GEO Writer tasks, team members) and the published API rate limits. Limits resolve through the account owner, so a team member sees the capacity that applies to them. An unlimited quota returns limit and remaining as null with unlimited set to true, since Infinity is not representable in JSON. The subscription block is only present for callers who can access Billing and Plans in the app (the account owner, or a team member with billing access); everyone else gets the same response without that key. requests_per_minute is the ceiling of the key used for the call, not a fixed number. For a key limited to some projects, the response carries nothing about the rest of the account: plan, plan_name, subscription and limits.team_members are absent, api_key_project_ids lists the key's projects, limits.prompts.used counts those projects' prompts, limits.prompts and limits.intelligence_tasks show only remaining and unlimited (the capacity the key can still spend, without the account total), and the projects quota is capped at the projects it reaches. tracking_frequency stays, as the cadence those projects' data is collected at.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.get_account200_response import GetAccount200Response
from llmpulse.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.llmpulse.ai/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = llmpulse.Configuration(
    host = "https://api.llmpulse.ai/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: BearerAuth
configuration = llmpulse.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with llmpulse.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = llmpulse.AccountApi(api_client)

    try:
        # Account plan, quota usage and rate limits
        api_response = api_instance.get_account()
        print("The response of AccountApi->get_account:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->get_account: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetAccount200Response**](GetAccount200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Account usage snapshot |  -  |
**401** | Authentication failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

