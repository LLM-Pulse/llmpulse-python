# llmpulse.APIKeysApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_api_key**](APIKeysApi.md#create_api_key) | **POST** /api_keys | Create an API key limited to projects
[**list_api_keys**](APIKeysApi.md#list_api_keys) | **GET** /api_keys | List API keys
[**revoke_api_key**](APIKeysApi.md#revoke_api_key) | **DELETE** /api_keys/{id} | Revoke an API key


# **create_api_key**
> CreateApiKey201Response create_api_key(create_api_key_request)

Create an API key limited to projects

Creates an API key limited to the projects in project_ids, owned by the same user as the calling key, and returns its secret token once: store it, since it cannot be read again. The key sees only those projects (any other project answers ERR_PROJECT_NOT_FOUND) and cannot act on the whole account, and the set of projects never changes. This endpoint never creates an account-wide key; create one in the app under API Keys. scope is read (default) or read_write. Every project must be one the caller can access: a project of another account, a deleted one or an unknown id answers ERR_PROJECT_NOT_FOUND and nothing is created. A user can hold up to 500 active keys; past that the request answers ERR_LIMIT_REACHED until a key is revoked. Requires an account-wide `read_write` scope API key on the Scale plan or above: a key limited to some projects answers ERR_KEY_PROJECT_SCOPED. A team member needs permission to create API keys and can only choose projects they can access.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.create_api_key201_response import CreateApiKey201Response
from llmpulse.models.create_api_key_request import CreateApiKeyRequest
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
    api_instance = llmpulse.APIKeysApi(api_client)
    create_api_key_request = llmpulse.CreateApiKeyRequest() # CreateApiKeyRequest | 

    try:
        # Create an API key limited to projects
        api_response = api_instance.create_api_key(create_api_key_request)
        print("The response of APIKeysApi->create_api_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling APIKeysApi->create_api_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_api_key_request** | [**CreateApiKeyRequest**](CreateApiKeyRequest.md)|  | 

### Return type

[**CreateApiKey201Response**](CreateApiKey201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created. The key as GET /api_keys lists it, plus its secret token, returned only this once. |  -  |
**401** | Authentication failed |  -  |
**403** | A key limited to some projects answers ERR_KEY_PROJECT_SCOPED and a read-only key ERR_INSUFFICIENT_SCOPE: managing keys needs an account-wide read and write key. A team member without the API Keys permission answers ERR_INSUFFICIENT_PERMISSION, and creating a key below the Scale plan ERR_PLAN_REQUIRED, with the same status |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_api_keys**
> ListApiKeys200Response list_api_keys(page=page, per_page=per_page)

List API keys

Lists the API keys of the user the calling key belongs to, newest first, revoked ones included: name, the visible prefix of the token, scope (read or read_write), the projects a key is limited to (project_scoped, project_ids; an empty list on an account-wide key), when it was created and last used, and when it was revoked. The secret token is only ever returned once, by POST /api_keys. Requires an account-wide `read_write` scope API key: a key limited to some projects answers ERR_KEY_PROJECT_SCOPED. Still answers after the account moves below the Scale plan, so old keys can be found and revoked. A team member needs the API Keys permission and sees only their own keys.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.list_api_keys200_response import ListApiKeys200Response
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
    api_instance = llmpulse.APIKeysApi(api_client)
    page = 56 # int |  (optional)
    per_page = 56 # int | Default 20, max 100 (optional)

    try:
        # List API keys
        api_response = api_instance.list_api_keys(page=page, per_page=per_page)
        print("The response of APIKeysApi->list_api_keys:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling APIKeysApi->list_api_keys: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **per_page** | **int**| Default 20, max 100 | [optional] 

### Return type

[**ListApiKeys200Response**](ListApiKeys200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**401** | Authentication failed |  -  |
**403** | A key limited to some projects answers ERR_KEY_PROJECT_SCOPED and a read-only key ERR_INSUFFICIENT_SCOPE: managing keys needs an account-wide read and write key. A team member without the API Keys permission answers ERR_INSUFFICIENT_PERMISSION, and creating a key below the Scale plan ERR_PLAN_REQUIRED, with the same status |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **revoke_api_key**
> RevokeApiKey200Response revoke_api_key(id)

Revoke an API key

Revokes an API key of the user the calling key belongs to: it stops working immediately and cannot be restored. Revoking a key that is already revoked answers the same way and keeps its original revocation time. A key of another user answers ERR_NOT_FOUND. The calling key can revoke itself. Requires an account-wide `read_write` scope API key: a key limited to some projects answers ERR_KEY_PROJECT_SCOPED. Still answers after the account moves below the Scale plan. A team member needs permission to delete API keys.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.revoke_api_key200_response import RevokeApiKey200Response
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
    api_instance = llmpulse.APIKeysApi(api_client)
    id = 56 # int | The key id from GET /api_keys

    try:
        # Revoke an API key
        api_response = api_instance.revoke_api_key(id)
        print("The response of APIKeysApi->revoke_api_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling APIKeysApi->revoke_api_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The key id from GET /api_keys | 

### Return type

[**RevokeApiKey200Response**](RevokeApiKey200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**401** | Authentication failed |  -  |
**403** | A key limited to some projects answers ERR_KEY_PROJECT_SCOPED and a read-only key ERR_INSUFFICIENT_SCOPE: managing keys needs an account-wide read and write key. A team member without the API Keys permission answers ERR_INSUFFICIENT_PERMISSION, and creating a key below the Scale plan ERR_PLAN_REQUIRED, with the same status |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

