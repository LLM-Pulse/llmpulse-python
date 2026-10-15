# llmpulse.PromptsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accept_suggested_prompts**](PromptsApi.md#accept_suggested_prompts) | **POST** /suggested_prompts/accept | Accept suggested prompts
[**create_prompt_generation**](PromptsApi.md#create_prompt_generation) | **POST** /prompt_generations | Generate prompt suggestions
[**create_prompts**](PromptsApi.md#create_prompts) | **POST** /prompts | Bulk-create prompts
[**delete_prompt**](PromptsApi.md#delete_prompt) | **DELETE** /prompts/{id} | Delete a prompt
[**get_prompt_generation**](PromptsApi.md#get_prompt_generation) | **GET** /prompt_generations/{id} | Get a prompt generation run
[**import_prompts**](PromptsApi.md#import_prompts) | **POST** /prompts/import | Import prompts
[**list_prompt_executions**](PromptsApi.md#list_prompt_executions) | **GET** /dimensions/prompt_executions | List prompt executions
[**list_prompts**](PromptsApi.md#list_prompts) | **GET** /dimensions/prompts | List prompts
[**list_query_fan_outs**](PromptsApi.md#list_query_fan_outs) | **GET** /dimensions/query_fan_outs | List query fan-out
[**list_suggested_prompts**](PromptsApi.md#list_suggested_prompts) | **GET** /suggested_prompts | List suggested prompts
[**reject_suggested_prompts**](PromptsApi.md#reject_suggested_prompts) | **POST** /suggested_prompts/reject | Reject suggested prompts
[**update_prompt**](PromptsApi.md#update_prompt) | **PATCH** /prompts/{id} | Edit a prompt&#39;s categorization


# **accept_suggested_prompts**
> SuggestedPromptsAcceptResponse accept_suggested_prompts(suggested_prompts_accept_request)

Accept suggested prompts

Starts tracking up to 100 pending suggestions: each becomes a prompt in its own country and language, optionally put in one tag (tag_ids or tag_names; create_missing creates a missing name when the team member may create tags). Suggestions that are no longer pending come back in skipped. When the new prompts would exceed the plan the call returns ERR_LIMIT_REACHED and accepts nothing. Requires a `read_write` scope API key and, for team members, create access to Prompts.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.suggested_prompts_accept_request import SuggestedPromptsAcceptRequest
from llmpulse.models.suggested_prompts_accept_response import SuggestedPromptsAcceptResponse
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
    api_instance = llmpulse.PromptsApi(api_client)
    suggested_prompts_accept_request = llmpulse.SuggestedPromptsAcceptRequest() # SuggestedPromptsAcceptRequest | 

    try:
        # Accept suggested prompts
        api_response = api_instance.accept_suggested_prompts(suggested_prompts_accept_request)
        print("The response of PromptsApi->accept_suggested_prompts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PromptsApi->accept_suggested_prompts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **suggested_prompts_accept_request** | [**SuggestedPromptsAcceptRequest**](SuggestedPromptsAcceptRequest.md)|  | 

### Return type

[**SuggestedPromptsAcceptResponse**](SuggestedPromptsAcceptResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Accepted and skipped suggestions |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_prompt_generation**
> PromptGenerationResponse create_prompt_generation(prompt_generation_request)

Generate prompt suggestions

Starts a suggestion run with one of the generators behind the app's Add prompts wizards and answers 202 with the run. website writes suggestions from the scraped website (80% non-brand, 20% brand; up to 100 per project, then ERR_LIMIT_REACHED), keyword from a keyword or the project profile (optionally around a competitor), topic from a topic, reddit from Reddit discussions of a topic or brand, paa from Google People Also Ask (up to 5 keywords, counted against the account's 24-hour lookup allowance), reputational from brand reputation questions, translate from the project's prompts of another locale, search_console from the connected property's top queries of the last 28 days (Growth plan or above, ERR_PLAN_REQUIRED). The suggestions land in the Suggested prompts queue; poll GET /prompt_generations/{id}, then accept the ones you want with POST /suggested_prompts/accept. Nothing is tracked until accepted. The request is validated before the run starts, and refused with ERR_LIMIT_REACHED when the plan has no prompt slot left, or ERR_QUOTA_EXCEEDED after 60 runs in an hour (the per-user prompt suggestion allowance, shared with project setup). Requires a `read_write` scope API key and, for team members, create access to Prompts.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.prompt_generation_request import PromptGenerationRequest
from llmpulse.models.prompt_generation_response import PromptGenerationResponse
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
    api_instance = llmpulse.PromptsApi(api_client)
    prompt_generation_request = llmpulse.PromptGenerationRequest() # PromptGenerationRequest | 

    try:
        # Generate prompt suggestions
        api_response = api_instance.create_prompt_generation(prompt_generation_request)
        print("The response of PromptsApi->create_prompt_generation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PromptsApi->create_prompt_generation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **prompt_generation_request** | [**PromptGenerationRequest**](PromptGenerationRequest.md)|  | 

### Return type

[**PromptGenerationResponse**](PromptGenerationResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | The run, status processing |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_prompts**
> PromptsCreateResponse create_prompts(prompts_create_request)

Bulk-create prompts

Add prompts to a project in bulk (up to 100 per request). Validates the account prompt quota and skips duplicates. Requires a `read_write` scope API key.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.prompts_create_request import PromptsCreateRequest
from llmpulse.models.prompts_create_response import PromptsCreateResponse
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
    api_instance = llmpulse.PromptsApi(api_client)
    prompts_create_request = llmpulse.PromptsCreateRequest() # PromptsCreateRequest | 

    try:
        # Bulk-create prompts
        api_response = api_instance.create_prompts(prompts_create_request)
        print("The response of PromptsApi->create_prompts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PromptsApi->create_prompts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **prompts_create_request** | [**PromptsCreateRequest**](PromptsCreateRequest.md)|  | 

### Return type

[**PromptsCreateResponse**](PromptsCreateResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created |  -  |
**403** | API key lacks write permission |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_prompt**
> delete_prompt(project_id, id)

Delete a prompt

Deletes a prompt (irreversible). The prompt disappears immediately and frees a prompt slot; its historical data (executions, mentions, citations, sentiment) is purged by a background job. Requires a `read_write` scope API key.

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
    api_instance = llmpulse.PromptsApi(api_client)
    project_id = 56 # int | Project ID
    id = 56 # int | 

    try:
        # Delete a prompt
        api_instance.delete_prompt(project_id, id)
    except Exception as e:
        print("Exception when calling PromptsApi->delete_prompt: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **id** | **int**|  | 

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
**200** | Deleted |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_prompt_generation**
> PromptGenerationResponse get_prompt_generation(project_id, id)

Get a prompt generation run

Returns a run started with POST /prompt_generations: processing while the generator works, then completed with the suggestions it saved to the Suggested prompts queue, or failed with an error code and message. Poll every few seconds; most runs finish within a minute. Runs are kept for 24 hours, their suggestions stay in the queue.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.prompt_generation_response import PromptGenerationResponse
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
    api_instance = llmpulse.PromptsApi(api_client)
    project_id = 56 # int | Project ID
    id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 

    try:
        # Get a prompt generation run
        api_response = api_instance.get_prompt_generation(project_id, id)
        print("The response of PromptsApi->get_prompt_generation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PromptsApi->get_prompt_generation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **id** | **UUID**|  | 

### Return type

[**PromptGenerationResponse**](PromptGenerationResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The run |  -  |
**403** | API key belongs to a team member whose permission matrix does not grant this feature |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **import_prompts**
> PromptsImportResponse import_prompts(prompts_import_request)

Import prompts

The app's CSV import as JSON: up to 500 rows, each with its own prompt, country_code, language_code (codes or names; both default to the project's) and tags, created when missing. Duplicates are skipped and existing prompts still get the row's tags. The prompt limits are checked before anything is written: when the new prompts would exceed the plan the call returns ERR_LIMIT_REACHED and imports nothing. Rows with an unknown country or language come back in row_errors. Responds 201 when it created prompts, 200 otherwise. Requires a `read_write` scope API key and, for team members, create access to Prompts.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.prompts_import_request import PromptsImportRequest
from llmpulse.models.prompts_import_response import PromptsImportResponse
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
    api_instance = llmpulse.PromptsApi(api_client)
    prompts_import_request = llmpulse.PromptsImportRequest() # PromptsImportRequest | 

    try:
        # Import prompts
        api_response = api_instance.import_prompts(prompts_import_request)
        print("The response of PromptsApi->import_prompts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PromptsApi->import_prompts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **prompts_import_request** | [**PromptsImportRequest**](PromptsImportRequest.md)|  | 

### Return type

[**PromptsImportResponse**](PromptsImportResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Nothing new was created (every row was a duplicate) |  -  |
**201** | Prompts imported |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_prompt_executions**
> PromptExecutionsResponse list_prompt_executions(project_id, page=page, per_page=per_page, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, var_from=var_from, to=to, mention_filter=mention_filter, citation_filter=citation_filter, competitors=competitors, output=output)

List prompt executions

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.prompt_executions_response import PromptExecutionsResponse
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
    api_instance = llmpulse.PromptsApi(api_client)
    project_id = 56 # int | Project ID
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    model = 'model_example' # str | Filter by one AI model. It must be a model enabled for the API key's user: an unknown value, or a model the user has not enabled, returns 422 ERR_INVALID_PARAM with the valid values in the message. (optional)
    collection_id = '12,34' # str | One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    prompt = 56 # int | Filter by prompt ID (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    mention_filter = 'mention_filter_example' # str | Filter by which brands are mentioned, as a two-axis matrix (your brand x competitors): mentions_you / not_mentions_you, mentions_competitor / not_mentions_competitor, and the four combined cells you_and_competitor, competitor_not_you (a rival wins and you are absent), you_not_competitor, no_brands (no tracked brand appears, i.e. open space). Combine with 'competitors' to narrow the competitor side to specific rivals; on a negative cell that reads 'none of these'. On /dimensions/sources it applies to the crawled content of each cited page instead of the answer text. The legacy value 'competitors_only' is still accepted as an alias of competitor_not_you. (optional)
    citation_filter = 'citation_filter_example' # str | Same two-axis matrix applied to the domains cited in the answer instead of the brands named in it. Independent of mention_filter; pass both to intersect them (e.g. mentions_you + not_cites_you finds answers that talk about you without linking to you). (optional)
    competitors = 'competitors_example' # str | Comma-separated competitor IDs (unknown IDs return ERR_INVALID_PARAM) (optional)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List prompt executions
        api_response = api_instance.list_prompt_executions(project_id, page=page, per_page=per_page, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, var_from=var_from, to=to, mention_filter=mention_filter, citation_filter=citation_filter, competitors=competitors, output=output)
        print("The response of PromptsApi->list_prompt_executions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PromptsApi->list_prompt_executions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **model** | **str**| Filter by one AI model. It must be a model enabled for the API key&#39;s user: an unknown value, or a model the user has not enabled, returns 422 ERR_INVALID_PARAM with the valid values in the message. | [optional] 
 **collection_id** | **str**| One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **prompt** | **int**| Filter by prompt ID | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **mention_filter** | **str**| Filter by which brands are mentioned, as a two-axis matrix (your brand x competitors): mentions_you / not_mentions_you, mentions_competitor / not_mentions_competitor, and the four combined cells you_and_competitor, competitor_not_you (a rival wins and you are absent), you_not_competitor, no_brands (no tracked brand appears, i.e. open space). Combine with &#39;competitors&#39; to narrow the competitor side to specific rivals; on a negative cell that reads &#39;none of these&#39;. On /dimensions/sources it applies to the crawled content of each cited page instead of the answer text. The legacy value &#39;competitors_only&#39; is still accepted as an alias of competitor_not_you. | [optional] 
 **citation_filter** | **str**| Same two-axis matrix applied to the domains cited in the answer instead of the brands named in it. Independent of mention_filter; pass both to intersect them (e.g. mentions_you + not_cites_you finds answers that talk about you without linking to you). | [optional] 
 **competitors** | **str**| Comma-separated competitor IDs (unknown IDs return ERR_INVALID_PARAM) | [optional] 
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

[**PromptExecutionsResponse**](PromptExecutionsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated executions. Every row carries app_url, the link that opens the answer in the app |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_prompts**
> PromptsResponse list_prompts(project_id, page=page, per_page=per_page, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, prompt_type=prompt_type, brand_kind=brand_kind, var_from=var_from, to=to, output=output)

List prompts

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.prompts_response import PromptsResponse
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
    api_instance = llmpulse.PromptsApi(api_client)
    project_id = 56 # int | Project ID
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    model = 'model_example' # str | Keep only the prompts with at least one execution on this AI model, of any outcome and date (the prompts /dimensions/prompt_executions lists for the same model). Prompts have no model of their own, so a prompt with no execution on this model yet (a newly enabled model, or a locale the model does not cover) is left out. An unknown value, or a model the API key's user has not enabled, returns 422 ERR_INVALID_PARAM. from and to still filter prompt creation. (optional)
    collection_id = '12,34' # str | One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    prompt = 56 # int | Filter by prompt ID (optional)
    prompt_type = 'prompt_type_example' # str | One prompt type or a comma-separated list: informational, navigational, commercial, transactional (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List prompts
        api_response = api_instance.list_prompts(project_id, page=page, per_page=per_page, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, prompt_type=prompt_type, brand_kind=brand_kind, var_from=var_from, to=to, output=output)
        print("The response of PromptsApi->list_prompts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PromptsApi->list_prompts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **model** | **str**| Keep only the prompts with at least one execution on this AI model, of any outcome and date (the prompts /dimensions/prompt_executions lists for the same model). Prompts have no model of their own, so a prompt with no execution on this model yet (a newly enabled model, or a locale the model does not cover) is left out. An unknown value, or a model the API key&#39;s user has not enabled, returns 422 ERR_INVALID_PARAM. from and to still filter prompt creation. | [optional] 
 **collection_id** | **str**| One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **prompt** | **int**| Filter by prompt ID | [optional] 
 **prompt_type** | **str**| One prompt type or a comma-separated list: informational, navigational, commercial, transactional | [optional] 
 **brand_kind** | **str**| Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

[**PromptsResponse**](PromptsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated prompts. Every row carries app_url, the link that opens the prompt in the app |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_query_fan_outs**
> list_query_fan_outs(project_id, page=page, per_page=per_page, view=view, order=order, direction=direction, query=query, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, prompt_type=prompt_type, brand_kind=brand_kind, range=range, var_from=var_from, to=to, output=output)

List query fan-out

The sub-queries a model actually issued when answering your tracked prompts. view=query (default) returns one row per distinct sub-query with count and share of all occurrences; view=prompt returns one row per prompt with how many distinct sub-queries it produced. Fan-out is reported mainly by ChatGPT, so an empty result usually means the models in scope do not expose it. The API returns the aggregation only: for a period-over-period delta, call it twice with explicit from/to.

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
    api_instance = llmpulse.PromptsApi(api_client)
    project_id = 56 # int | Project ID
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    view = 'query' # str | Row shape: one per distinct sub-query, or one per prompt (optional) (default to 'query')
    order = 'order_example' # str | Sort field; the allowed set depends on view (optional)
    direction = 'desc' # str |  (optional) (default to 'desc')
    query = 'query_example' # str | Case-insensitive substring filter on the sub-query text (optional)
    model = 'model_example' # str | Filter by one AI model. It must be a model enabled for the API key's user: an unknown value, or a model the user has not enabled, returns 422 ERR_INVALID_PARAM with the valid values in the message. (optional)
    collection_id = '12,34' # str | One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    prompt = 56 # int | Filter by prompt ID (optional)
    prompt_type = 'prompt_type_example' # str | One prompt type or a comma-separated list: informational, navigational, commercial, transactional (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    range = 56 # int | Number of days to look back (alternative to from/to) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List query fan-out
        api_instance.list_query_fan_outs(project_id, page=page, per_page=per_page, view=view, order=order, direction=direction, query=query, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, prompt_type=prompt_type, brand_kind=brand_kind, range=range, var_from=var_from, to=to, output=output)
    except Exception as e:
        print("Exception when calling PromptsApi->list_query_fan_outs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **view** | **str**| Row shape: one per distinct sub-query, or one per prompt | [optional] [default to &#39;query&#39;]
 **order** | **str**| Sort field; the allowed set depends on view | [optional] 
 **direction** | **str**|  | [optional] [default to &#39;desc&#39;]
 **query** | **str**| Case-insensitive substring filter on the sub-query text | [optional] 
 **model** | **str**| Filter by one AI model. It must be a model enabled for the API key&#39;s user: an unknown value, or a model the user has not enabled, returns 422 ERR_INVALID_PARAM with the valid values in the message. | [optional] 
 **collection_id** | **str**| One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **prompt** | **int**| Filter by prompt ID | [optional] 
 **prompt_type** | **str**| One prompt type or a comma-separated list: informational, navigational, commercial, transactional | [optional] 
 **brand_kind** | **str**| Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. | [optional] 
 **range** | **int**| Number of days to look back (alternative to from/to) | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

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
**200** | Paginated fan-out rows |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_suggested_prompts**
> SuggestedPromptsResponse list_suggested_prompts(project_id, source=source, status=status, page=page, per_page=per_page)

List suggested prompts

Lists the project's Suggested prompts queue, the same list the app's Suggested Prompts tab shows, oldest first. It holds the suggestions of every generator (website, magic for keyword runs, topic, reddit, paa, reputational, translate, gsc for Search Console, catalog). Pending suggestions by default; status=all also returns accepted (with the prompt they became) and rejected ones. Team members need create access to Prompts, like the app's tab.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.suggested_prompts_response import SuggestedPromptsResponse
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
    api_instance = llmpulse.PromptsApi(api_client)
    project_id = 56 # int | Project ID
    source = 'source_example' # str | Only suggestions from this generator (optional)
    status = 'pending' # str | Only suggestions in this status (optional) (default to 'pending')
    page = 1 # int |  (optional) (default to 1)
    per_page = 50 # int |  (optional) (default to 50)

    try:
        # List suggested prompts
        api_response = api_instance.list_suggested_prompts(project_id, source=source, status=status, page=page, per_page=per_page)
        print("The response of PromptsApi->list_suggested_prompts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PromptsApi->list_suggested_prompts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **source** | **str**| Only suggestions from this generator | [optional] 
 **status** | **str**| Only suggestions in this status | [optional] [default to &#39;pending&#39;]
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 50]

### Return type

[**SuggestedPromptsResponse**](SuggestedPromptsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated suggestions |  -  |
**403** | API key belongs to a team member whose permission matrix does not grant this feature |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reject_suggested_prompts**
> SuggestedPromptsRejectResponse reject_suggested_prompts(suggested_prompt_ids_request)

Reject suggested prompts

Marks up to 100 pending suggestions as rejected, so they leave the pending list; suggestions that are no longer pending stay as they are. Tracks and deletes nothing. Requires a `read_write` scope API key and, for team members, create access to Prompts.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.suggested_prompt_ids_request import SuggestedPromptIdsRequest
from llmpulse.models.suggested_prompts_reject_response import SuggestedPromptsRejectResponse
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
    api_instance = llmpulse.PromptsApi(api_client)
    suggested_prompt_ids_request = llmpulse.SuggestedPromptIdsRequest() # SuggestedPromptIdsRequest | 

    try:
        # Reject suggested prompts
        api_response = api_instance.reject_suggested_prompts(suggested_prompt_ids_request)
        print("The response of PromptsApi->reject_suggested_prompts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PromptsApi->reject_suggested_prompts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **suggested_prompt_ids_request** | [**SuggestedPromptIdsRequest**](SuggestedPromptIdsRequest.md)|  | 

### Return type

[**SuggestedPromptsRejectResponse**](SuggestedPromptsRejectResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The suggestions rejected |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_prompt**
> PromptCategorizationResponse update_prompt(id, update_prompt_request)

Edit a prompt's categorization

Manual categorization, exactly like editing the intent and brand badges on the prompt page: send `prompt_type`, `brand_kind` or both. The prompt is marked as manually categorized (`categorization_source` becomes `manual`), so automatic categorization no longer changes it; the prompt page can revert it to automatic. Any other field returns ERR_INVALID_PARAM. Not available from a white-label portal (ERR_INTEGRATION_UNAVAILABLE), where the page hides the editor. Requires a `read_write` scope API key and, for team members, update permission on Prompts.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.prompt_categorization_response import PromptCategorizationResponse
from llmpulse.models.update_prompt_request import UpdatePromptRequest
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
    api_instance = llmpulse.PromptsApi(api_client)
    id = 56 # int | 
    update_prompt_request = llmpulse.UpdatePromptRequest() # UpdatePromptRequest | 

    try:
        # Edit a prompt's categorization
        api_response = api_instance.update_prompt(id, update_prompt_request)
        print("The response of PromptsApi->update_prompt:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PromptsApi->update_prompt: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  | 
 **update_prompt_request** | [**UpdatePromptRequest**](UpdatePromptRequest.md)|  | 

### Return type

[**PromptCategorizationResponse**](PromptCategorizationResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The prompt with its new categorization |  -  |
**403** | Writes with a read-only key answer ERR_INSUFFICIENT_SCOPE, a team member without the permission ERR_INSUFFICIENT_PERMISSION, and a request made on a white-label portal host, where the app does not offer this action, ERR_INTEGRATION_UNAVAILABLE, with the same status |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

