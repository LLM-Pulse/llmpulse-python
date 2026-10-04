# llmpulse.StoreIntegrationsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accept_catalog_prompt_suggestions**](StoreIntegrationsApi.md#accept_catalog_prompt_suggestions) | **POST** /catalog_prompt_suggestions/accept | Accept catalog prompt suggestions
[**create_catalog_prompt_suggestions**](StoreIntegrationsApi.md#create_catalog_prompt_suggestions) | **POST** /catalog_prompt_suggestions | Suggest buyer prompts from catalog products
[**get_store_connection**](StoreIntegrationsApi.md#get_store_connection) | **GET** /store_connection | Match a store to a project
[**list_ai_orders**](StoreIntegrationsApi.md#list_ai_orders) | **GET** /ai_orders | Read AI-referred store orders
[**list_catalog_prompt_suggestions**](StoreIntegrationsApi.md#list_catalog_prompt_suggestions) | **GET** /catalog_prompt_suggestions | List catalog prompt suggestions
[**reject_catalog_prompt_suggestions**](StoreIntegrationsApi.md#reject_catalog_prompt_suggestions) | **POST** /catalog_prompt_suggestions/reject | Reject catalog prompt suggestions
[**replace_ai_orders**](StoreIntegrationsApi.md#replace_ai_orders) | **PUT** /ai_orders | Replace AI-referred store orders for a window


# **accept_catalog_prompt_suggestions**
> CatalogPromptSuggestionsAcceptResponse accept_catalog_prompt_suggestions(catalog_prompt_suggestion_ids_request)

Accept catalog prompt suggestions

Starts tracking pending suggestions: each one becomes a prompt, tagged with a collection named after its product. Suggestions that are no longer pending come back in skipped. All accepted suggestions must share one country and language. When the new prompts would exceed the plan, the call returns ERR_LIMIT_REACHED and accepts nothing. Requires a `read_write` scope API key and, for team members, create access to Prompts. Not available to accounts with a white-label portal or an embed (ERR_INTEGRATION_UNAVAILABLE).

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.catalog_prompt_suggestion_ids_request import CatalogPromptSuggestionIdsRequest
from llmpulse.models.catalog_prompt_suggestions_accept_response import CatalogPromptSuggestionsAcceptResponse
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
    api_instance = llmpulse.StoreIntegrationsApi(api_client)
    catalog_prompt_suggestion_ids_request = llmpulse.CatalogPromptSuggestionIdsRequest() # CatalogPromptSuggestionIdsRequest | 

    try:
        # Accept catalog prompt suggestions
        api_response = api_instance.accept_catalog_prompt_suggestions(catalog_prompt_suggestion_ids_request)
        print("The response of StoreIntegrationsApi->accept_catalog_prompt_suggestions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoreIntegrationsApi->accept_catalog_prompt_suggestions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **catalog_prompt_suggestion_ids_request** | [**CatalogPromptSuggestionIdsRequest**](CatalogPromptSuggestionIdsRequest.md)|  | 

### Return type

[**CatalogPromptSuggestionsAcceptResponse**](CatalogPromptSuggestionsAcceptResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Accepted and skipped suggestions |  -  |
**403** | The account has a white-label portal or an embed, so store integrations are not available (ERR_INTEGRATION_UNAVAILABLE). Writes with a read-only key answer ERR_INSUFFICIENT_SCOPE, and a team member without the permission ERR_INSUFFICIENT_PERMISSION, with the same status |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_catalog_prompt_suggestions**
> CatalogPromptSuggestionsCreateResponse create_catalog_prompt_suggestions(catalog_prompt_suggestions_create_request)

Suggest buyer prompts from catalog products

Writes buyer prompts for up to 20 catalog products and saves them as pending suggestions in the project's Suggested prompts queue, with the product recorded on each. Generation draws on the hourly prompt-suggestion allowance the app also uses (ERR_QUOTA_EXCEEDED once it is used up); a failed generation returns ERR_GENERATION_FAILED (502) and can be retried. Requires a `read_write` scope API key and, for team members, create access to Prompts. Not available to accounts with a white-label portal or an embed (ERR_INTEGRATION_UNAVAILABLE).

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.catalog_prompt_suggestions_create_request import CatalogPromptSuggestionsCreateRequest
from llmpulse.models.catalog_prompt_suggestions_create_response import CatalogPromptSuggestionsCreateResponse
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
    api_instance = llmpulse.StoreIntegrationsApi(api_client)
    catalog_prompt_suggestions_create_request = llmpulse.CatalogPromptSuggestionsCreateRequest() # CatalogPromptSuggestionsCreateRequest | 

    try:
        # Suggest buyer prompts from catalog products
        api_response = api_instance.create_catalog_prompt_suggestions(catalog_prompt_suggestions_create_request)
        print("The response of StoreIntegrationsApi->create_catalog_prompt_suggestions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoreIntegrationsApi->create_catalog_prompt_suggestions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **catalog_prompt_suggestions_create_request** | [**CatalogPromptSuggestionsCreateRequest**](CatalogPromptSuggestionsCreateRequest.md)|  | 

### Return type

[**CatalogPromptSuggestionsCreateResponse**](CatalogPromptSuggestionsCreateResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The suggestions saved for these products |  -  |
**403** | The account has a white-label portal or an embed, so store integrations are not available (ERR_INTEGRATION_UNAVAILABLE). Writes with a read-only key answer ERR_INSUFFICIENT_SCOPE, and a team member without the permission ERR_INSUFFICIENT_PERMISSION, with the same status |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |
**502** | The AI generation failed; retry the request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_store_connection**
> StoreConnectionResponse get_store_connection(platform, domain)

Match a store to a project

Tells a store app whether the API key's account can use it and which project the store belongs to: the live project whose domain equals the store domain, else one whose domain is a parent or a subdomain of it, else null. candidates lists every live project of the account so the app can offer a picker. Takes no project_id. Not available to accounts with a white-label portal or an embed (ERR_INTEGRATION_UNAVAILABLE).

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.store_connection_response import StoreConnectionResponse
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
    api_instance = llmpulse.StoreIntegrationsApi(api_client)
    platform = 'platform_example' # str | Store platform
    domain = 'domain_example' # str | Store domain, with or without scheme, e.g. acme-store.com

    try:
        # Match a store to a project
        api_response = api_instance.get_store_connection(platform, domain)
        print("The response of StoreIntegrationsApi->get_store_connection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoreIntegrationsApi->get_store_connection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platform** | **str**| Store platform | 
 **domain** | **str**| Store domain, with or without scheme, e.g. acme-store.com | 

### Return type

[**StoreConnectionResponse**](StoreConnectionResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Eligibility, the matching project and the candidates |  -  |
**403** | The account has a white-label portal or an embed, so store integrations are not available (ERR_INTEGRATION_UNAVAILABLE). Writes with a read-only key answer ERR_INSUFFICIENT_SCOPE, and a team member without the permission ERR_INSUFFICIENT_PERMISSION, with the same status |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_ai_orders**
> AiOrdersResponse list_ai_orders(project_id, platform=platform, var_from=var_from, to=to)

Read AI-referred store orders

Reads back the AI-referred orders a store app pushed for a project: totals, one row per AI assistant and a daily series of the days with orders. Revenue values are decimal strings in currency. Team members need read access to AI Traffic. Not available to accounts with a white-label portal or an embed (ERR_INTEGRATION_UNAVAILABLE).

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.ai_orders_response import AiOrdersResponse
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
    api_instance = llmpulse.StoreIntegrationsApi(api_client)
    project_id = 56 # int | Project ID
    platform = 'shopify' # str | Store platform (optional) (default to 'shopify')
    var_from = '2013-10-20' # date | First day (YYYY-MM-DD). Defaults to 89 days before to (optional)
    to = '2013-10-20' # date | Last day (YYYY-MM-DD). Defaults to today; the window is at most 400 days (optional)

    try:
        # Read AI-referred store orders
        api_response = api_instance.list_ai_orders(project_id, platform=platform, var_from=var_from, to=to)
        print("The response of StoreIntegrationsApi->list_ai_orders:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoreIntegrationsApi->list_ai_orders: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **platform** | **str**| Store platform | [optional] [default to &#39;shopify&#39;]
 **var_from** | **date**| First day (YYYY-MM-DD). Defaults to 89 days before to | [optional] 
 **to** | **date**| Last day (YYYY-MM-DD). Defaults to today; the window is at most 400 days | [optional] 

### Return type

[**AiOrdersResponse**](AiOrdersResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Totals, per-assistant rows and the daily series |  -  |
**403** | The account has a white-label portal or an embed, so store integrations are not available (ERR_INTEGRATION_UNAVAILABLE). Writes with a read-only key answer ERR_INSUFFICIENT_SCOPE, and a team member without the permission ERR_INSUFFICIENT_PERMISSION, with the same status |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_catalog_prompt_suggestions**
> CatalogPromptSuggestionsResponse list_catalog_prompt_suggestions(project_id, status=status, product_external_id=product_external_id, page=page, per_page=per_page)

List catalog prompt suggestions

Lists the buyer prompts suggested from a store catalog, oldest first, with their status and the product each one came from. Team members need read access to Prompts. Not available to accounts with a white-label portal or an embed (ERR_INTEGRATION_UNAVAILABLE).

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.catalog_prompt_suggestions_response import CatalogPromptSuggestionsResponse
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
    api_instance = llmpulse.StoreIntegrationsApi(api_client)
    project_id = 56 # int | Project ID
    status = 'status_example' # str | Only suggestions in this status (optional)
    product_external_id = 'product_external_id_example' # str | Only suggestions for this store product id (optional)
    page = 1 # int |  (optional) (default to 1)
    per_page = 50 # int |  (optional) (default to 50)

    try:
        # List catalog prompt suggestions
        api_response = api_instance.list_catalog_prompt_suggestions(project_id, status=status, product_external_id=product_external_id, page=page, per_page=per_page)
        print("The response of StoreIntegrationsApi->list_catalog_prompt_suggestions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoreIntegrationsApi->list_catalog_prompt_suggestions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **status** | **str**| Only suggestions in this status | [optional] 
 **product_external_id** | **str**| Only suggestions for this store product id | [optional] 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 50]

### Return type

[**CatalogPromptSuggestionsResponse**](CatalogPromptSuggestionsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated suggestions |  -  |
**403** | The account has a white-label portal or an embed, so store integrations are not available (ERR_INTEGRATION_UNAVAILABLE). Writes with a read-only key answer ERR_INSUFFICIENT_SCOPE, and a team member without the permission ERR_INSUFFICIENT_PERMISSION, with the same status |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reject_catalog_prompt_suggestions**
> CatalogPromptSuggestionsRejectResponse reject_catalog_prompt_suggestions(catalog_prompt_suggestion_ids_request)

Reject catalog prompt suggestions

Marks pending suggestions as rejected; suggestions that are no longer pending stay as they are. Requires a `read_write` scope API key and, for team members, update access to Prompts. Not available to accounts with a white-label portal or an embed (ERR_INTEGRATION_UNAVAILABLE).

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.catalog_prompt_suggestion_ids_request import CatalogPromptSuggestionIdsRequest
from llmpulse.models.catalog_prompt_suggestions_reject_response import CatalogPromptSuggestionsRejectResponse
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
    api_instance = llmpulse.StoreIntegrationsApi(api_client)
    catalog_prompt_suggestion_ids_request = llmpulse.CatalogPromptSuggestionIdsRequest() # CatalogPromptSuggestionIdsRequest | 

    try:
        # Reject catalog prompt suggestions
        api_response = api_instance.reject_catalog_prompt_suggestions(catalog_prompt_suggestion_ids_request)
        print("The response of StoreIntegrationsApi->reject_catalog_prompt_suggestions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoreIntegrationsApi->reject_catalog_prompt_suggestions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **catalog_prompt_suggestion_ids_request** | [**CatalogPromptSuggestionIdsRequest**](CatalogPromptSuggestionIdsRequest.md)|  | 

### Return type

[**CatalogPromptSuggestionsRejectResponse**](CatalogPromptSuggestionsRejectResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | How many suggestions were rejected |  -  |
**403** | The account has a white-label portal or an embed, so store integrations are not available (ERR_INTEGRATION_UNAVAILABLE). Writes with a read-only key answer ERR_INSUFFICIENT_SCOPE, and a team member without the permission ERR_INSUFFICIENT_PERMISSION, with the same status |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **replace_ai_orders**
> AiOrdersUpdateResponse replace_ai_orders(ai_orders_update_request)

Replace AI-referred store orders for a window

Replaces the daily AI-referred orders and revenue of the from..to window. Send the raw referring host or utm_source of each order's first visit as referrer: LLM Pulse classifies it and ignores anything that is not an AI assistant. Entries for the same day and assistant are summed. Every stored row of that project and platform inside the window is replaced, so pushing the same window again converges instead of counting twice. Rows are kept per project and platform, not per store, so one store reports per project. Requires a `read_write` scope API key and, for team members, update access to AI Traffic. Not available to accounts with a white-label portal or an embed (ERR_INTEGRATION_UNAVAILABLE).

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.ai_orders_update_request import AiOrdersUpdateRequest
from llmpulse.models.ai_orders_update_response import AiOrdersUpdateResponse
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
    api_instance = llmpulse.StoreIntegrationsApi(api_client)
    ai_orders_update_request = llmpulse.AiOrdersUpdateRequest() # AiOrdersUpdateRequest | 

    try:
        # Replace AI-referred store orders for a window
        api_response = api_instance.replace_ai_orders(ai_orders_update_request)
        print("The response of StoreIntegrationsApi->replace_ai_orders:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoreIntegrationsApi->replace_ai_orders: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ai_orders_update_request** | [**AiOrdersUpdateRequest**](AiOrdersUpdateRequest.md)|  | 

### Return type

[**AiOrdersUpdateResponse**](AiOrdersUpdateResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Rows stored and entries ignored |  -  |
**403** | The account has a white-label portal or an embed, so store integrations are not available (ERR_INTEGRATION_UNAVAILABLE). Writes with a read-only key answer ERR_INSUFFICIENT_SCOPE, and a team member without the permission ERR_INSUFFICIENT_PERMISSION, with the same status |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

