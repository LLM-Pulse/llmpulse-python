# llmpulse.GEOWriterApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_intelligence_task**](GEOWriterApi.md#create_intelligence_task) | **POST** /intelligence_tasks | Create a GEO Writer task
[**get_intelligence_task**](GEOWriterApi.md#get_intelligence_task) | **GET** /intelligence_tasks/{id} | Get a GEO Writer task
[**list_intelligence_tasks**](GEOWriterApi.md#list_intelligence_tasks) | **GET** /intelligence_tasks | List GEO Writer tasks
[**revert_intelligence_task_content**](GEOWriterApi.md#revert_intelligence_task_content) | **POST** /intelligence_tasks/{id}/revert | Revert GEO Writer task content
[**update_intelligence_task_content**](GEOWriterApi.md#update_intelligence_task_content) | **PATCH** /intelligence_tasks/{id} | Edit GEO Writer task content


# **create_intelligence_task**
> IntelligenceTask create_intelligence_task(intelligence_task_create_request)

Create a GEO Writer task

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.intelligence_task import IntelligenceTask
from llmpulse.models.intelligence_task_create_request import IntelligenceTaskCreateRequest
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
    api_instance = llmpulse.GEOWriterApi(api_client)
    intelligence_task_create_request = llmpulse.IntelligenceTaskCreateRequest() # IntelligenceTaskCreateRequest | 

    try:
        # Create a GEO Writer task
        api_response = api_instance.create_intelligence_task(intelligence_task_create_request)
        print("The response of GEOWriterApi->create_intelligence_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOWriterApi->create_intelligence_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **intelligence_task_create_request** | [**IntelligenceTaskCreateRequest**](IntelligenceTaskCreateRequest.md)|  | 

### Return type

[**IntelligenceTask**](IntelligenceTask.md)

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

# **get_intelligence_task**
> IntelligenceTask get_intelligence_task(project_id, id)

Get a GEO Writer task

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.intelligence_task import IntelligenceTask
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
    api_instance = llmpulse.GEOWriterApi(api_client)
    project_id = 56 # int | Project ID
    id = 'id_example' # str | Numeric task ID or public_id string token

    try:
        # Get a GEO Writer task
        api_response = api_instance.get_intelligence_task(project_id, id)
        print("The response of GEOWriterApi->get_intelligence_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOWriterApi->get_intelligence_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **id** | **str**| Numeric task ID or public_id string token | 

### Return type

[**IntelligenceTask**](IntelligenceTask.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Task with result_data when completed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_intelligence_tasks**
> list_intelligence_tasks(project_id, task_type=task_type, status=status, page=page, per_page=per_page)

List GEO Writer tasks

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
    api_instance = llmpulse.GEOWriterApi(api_client)
    project_id = 56 # int | Project ID
    task_type = 'task_type_example' # str |  (optional)
    status = 'status_example' # str |  (optional)
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)

    try:
        # List GEO Writer tasks
        api_instance.list_intelligence_tasks(project_id, task_type=task_type, status=status, page=page, per_page=per_page)
    except Exception as e:
        print("Exception when calling GEOWriterApi->list_intelligence_tasks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **task_type** | **str**|  | [optional] 
 **status** | **str**|  | [optional] 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated tasks |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **revert_intelligence_task_content**
> IntelligenceTask revert_intelligence_task_content(project_id, id)

Revert GEO Writer task content

Discards every manual edit on the task and restores the output exactly as it was generated. Returns ERR_INVALID_PARAM when the task has no manual edits. Requires a `read_write` scope API key and, for team members, update permission on GEO Writer.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.intelligence_task import IntelligenceTask
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
    api_instance = llmpulse.GEOWriterApi(api_client)
    project_id = 56 # int | Project ID
    id = 'id_example' # str | Numeric task ID or public_id string token

    try:
        # Revert GEO Writer task content
        api_response = api_instance.revert_intelligence_task_content(project_id, id)
        print("The response of GEOWriterApi->revert_intelligence_task_content:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOWriterApi->revert_intelligence_task_content: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **id** | **str**| Numeric task ID or public_id string token | 

### Return type

[**IntelligenceTask**](IntelligenceTask.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Task restored to its generated output |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_intelligence_task_content**
> IntelligenceTaskUpdateResponse update_intelligence_task_content(id, intelligence_task_update_request)

Edit GEO Writer task content

Edits the text of a completed task in place. `edits` maps dotted paths into result_data (for example `title` or `sections.0.content`) to replacement text. Only string fields that already exist can change: a path that does not resolve to text, a blank `title`, a value over 20,000 characters or an empty `edits` object is rejected with ERR_INVALID_PARAM and nothing is written. Values identical to the stored text are ignored, and the response lists the paths that actually changed. The first edit keeps a copy of the generated output so POST /intelligence_tasks/{id}/revert can restore it; regenerating the task replaces the edited content. Requires a `read_write` scope API key and, for team members, update permission on GEO Writer.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.intelligence_task_update_request import IntelligenceTaskUpdateRequest
from llmpulse.models.intelligence_task_update_response import IntelligenceTaskUpdateResponse
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
    api_instance = llmpulse.GEOWriterApi(api_client)
    id = 'id_example' # str | Numeric task ID or public_id string token
    intelligence_task_update_request = llmpulse.IntelligenceTaskUpdateRequest() # IntelligenceTaskUpdateRequest | 

    try:
        # Edit GEO Writer task content
        api_response = api_instance.update_intelligence_task_content(id, intelligence_task_update_request)
        print("The response of GEOWriterApi->update_intelligence_task_content:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOWriterApi->update_intelligence_task_content: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Numeric task ID or public_id string token | 
 **intelligence_task_update_request** | [**IntelligenceTaskUpdateRequest**](IntelligenceTaskUpdateRequest.md)|  | 

### Return type

[**IntelligenceTaskUpdateResponse**](IntelligenceTaskUpdateResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated task with the paths that changed |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

