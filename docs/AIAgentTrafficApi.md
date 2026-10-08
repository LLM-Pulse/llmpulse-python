# llmpulse.AIAgentTrafficApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_agent_traffic**](AIAgentTrafficApi.md#get_agent_traffic) | **GET** /metrics/agent_traffic | AI bot crawler traffic (Scale plan or above, Beta)
[**get_ai_traffic**](AIAgentTrafficApi.md#get_ai_traffic) | **GET** /metrics/ai_traffic | AI referral traffic (Scale plan or above)
[**list_agent_bots**](AIAgentTrafficApi.md#list_agent_bots) | **GET** /dimensions/agent_bots | AI bot catalog (Scale plan or above)


# **get_agent_traffic**
> AgentTrafficResponse get_agent_traffic(project_id, range=range, var_from=var_from, to=to, bot=bot, company=company, group_by=group_by, granularity=granularity)

AI bot crawler traffic (Scale plan or above, Beta)

Aggregated AI bot traffic hitting the project's origin server (GPTBot, PerplexityBot, ClaudeBot, OAI-SearchBot, Google-Extended, etc.). Sourced from Cloudflare or CSV uploads. Requires the Scale plan; lower tiers receive ERR_PLAN_REQUIRED.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.agent_traffic_response import AgentTrafficResponse
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
    api_instance = llmpulse.AIAgentTrafficApi(api_client)
    project_id = 56 # int | Project ID
    range = 56 # int | Number of days to look back (alternative to from/to) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    bot = 'bot_example' # str | Filter by bot slug (e.g. gptbot, claudebot, perplexitybot) (optional)
    company = 'company_example' # str | Filter by company (e.g. openai, anthropic, google) (optional)
    group_by = 'bot' # str |  (optional) (default to 'bot')
    granularity = 'granularity_example' # str |  (optional)

    try:
        # AI bot crawler traffic (Scale plan or above, Beta)
        api_response = api_instance.get_agent_traffic(project_id, range=range, var_from=var_from, to=to, bot=bot, company=company, group_by=group_by, granularity=granularity)
        print("The response of AIAgentTrafficApi->get_agent_traffic:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAgentTrafficApi->get_agent_traffic: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **range** | **int**| Number of days to look back (alternative to from/to) | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **bot** | **str**| Filter by bot slug (e.g. gptbot, claudebot, perplexitybot) | [optional] 
 **company** | **str**| Filter by company (e.g. openai, anthropic, google) | [optional] 
 **group_by** | **str**|  | [optional] [default to &#39;bot&#39;]
 **granularity** | **str**|  | [optional] 

### Return type

[**AgentTrafficResponse**](AgentTrafficResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Agent traffic data |  -  |
**403** | Endpoint requires a higher plan tier |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_ai_traffic**
> get_ai_traffic(project_id, range=range, var_from=var_from, to=to, source=source, granularity=granularity)

AI referral traffic (Scale plan or above)

AI referral traffic for a project: human visits arriving from AI assistants (ChatGPT, Perplexity, Gemini, Claude, etc.), measured from the connected web analytics provider (Google Analytics 4, Adobe Analytics, PostHog, Plausible, Matomo or Piano). Returns per-source users, sessions and conversions with totals and a conversion rate. Requires a connected provider and the Scale plan; otherwise returns ERR_AI_TRAFFIC_NOT_CONNECTED or ERR_PLAN_REQUIRED.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
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
    api_instance = llmpulse.AIAgentTrafficApi(api_client)
    project_id = 56 # int | Project ID
    range = 56 # int | Number of days to look back (alternative to from/to) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    source = 'source_example' # str | Filter by a single AI source slug (e.g. chatgpt, perplexity, gemini, claude) (optional)
    granularity = 'granularity_example' # str |  (optional)

    try:
        # AI referral traffic (Scale plan or above)
        api_instance.get_ai_traffic(project_id, range=range, var_from=var_from, to=to, source=source, granularity=granularity)
    except Exception as e:
        print("Exception when calling AIAgentTrafficApi->get_ai_traffic: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **range** | **int**| Number of days to look back (alternative to from/to) | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **source** | **str**| Filter by a single AI source slug (e.g. chatgpt, perplexity, gemini, claude) | [optional] 
 **granularity** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | AI referral traffic data |  -  |
**403** | Endpoint requires a higher plan tier |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_agent_bots**
> AgentBotsResponse list_agent_bots(project_id, output=output)

AI bot catalog (Scale plan or above)

Static catalog of AI bots that Agent Analytics can identify. Useful for rendering filter UIs that mirror our internal classification (slug, display name, company, category, Cloudflare verified-bot mapping, description). Requires the Scale plan; lower tiers receive ERR_PLAN_REQUIRED. The equivalent MCP tool list_agent_bots is available on the Scale plan or above.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.agent_bots_response import AgentBotsResponse
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
    api_instance = llmpulse.AIAgentTrafficApi(api_client)
    project_id = 56 # int | Project ID
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # AI bot catalog (Scale plan or above)
        api_response = api_instance.list_agent_bots(project_id, output=output)
        print("The response of AIAgentTrafficApi->list_agent_bots:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAgentTrafficApi->list_agent_bots: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

[**AgentBotsResponse**](AgentBotsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Bot catalog |  -  |
**403** | Endpoint requires a higher plan tier |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

