# llmpulse.ReputationStudiesApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_reputation_report**](ReputationStudiesApi.md#create_reputation_report) | **POST** /reputation/reports | Start a reputation report
[**get_reputation_report**](ReputationStudiesApi.md#get_reputation_report) | **GET** /reputation/reports/{id} | Get reputation report scores
[**get_study**](ReputationStudiesApi.md#get_study) | **GET** /studies/{id} | Get a custom AI study
[**get_study_report**](ReputationStudiesApi.md#get_study_report) | **GET** /studies/{id}/reports/{report_id} | Get custom study report scores
[**list_reputation_reports**](ReputationStudiesApi.md#list_reputation_reports) | **GET** /reputation/reports | List reputation reports
[**list_studies**](ReputationStudiesApi.md#list_studies) | **GET** /studies | List custom AI studies


# **create_reputation_report**
> ReputationReportCreateResponse create_reputation_report(create_reputation_report_request)

Start a reputation report

Starts this month's Brand Reputation report, like the Generate button on the Reputation page: 201 with the new report (status pending). When the month already holds a report that did not fail, whether it is still running or finished, nothing new starts and the answer is 200 with created false and that report. With recalculate true it uses the month's one manual recalculation instead (the Recalculate This Month button): a fresh run across every analyst model, 201 when it starts, 200 with created false while a report is still running, and ERR_LIMIT_REACHED once the month holds two reports. Generation runs in the background: poll GET /reputation/reports until status is completed, then read the scores with GET /reputation/reports/{id}. ERR_RATE_LIMITED (429, with Retry-After) means another request is starting a report for the same project; retry after a few seconds. recalculate must be true or false and unknown fields are refused (ERR_INVALID_PARAM). Requires reputation monitoring on the account, a `read_write` scope API key and, for team members, create permission on Reputation.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.create_reputation_report_request import CreateReputationReportRequest
from llmpulse.models.reputation_report_create_response import ReputationReportCreateResponse
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
    api_instance = llmpulse.ReputationStudiesApi(api_client)
    create_reputation_report_request = llmpulse.CreateReputationReportRequest() # CreateReputationReportRequest | 

    try:
        # Start a reputation report
        api_response = api_instance.create_reputation_report(create_reputation_report_request)
        print("The response of ReputationStudiesApi->create_reputation_report:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ReputationStudiesApi->create_reputation_report: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_reputation_report_request** | [**CreateReputationReportRequest**](CreateReputationReportRequest.md)|  | 

### Return type

[**ReputationReportCreateResponse**](ReputationReportCreateResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Nothing new started; the report that already holds this month |  -  |
**201** | The new report, status pending |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |
**429** | Another request is starting a report for this project; retry after a few seconds |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_reputation_report**
> get_reputation_report(id, project_id, page=page, per_page=per_page, model=model, brand=brand, dimension=dimension, output=output)

Get reputation report scores

One reputation report's scores as flat rows: one row per analyst model, brand, dimension and attribute, with its 0-100 score and the reasoning the model gave. Scores come from several analyst models independently, so compare models rather than averaging them blindly.

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
    api_instance = llmpulse.ReputationStudiesApi(api_client)
    id = 'id_example' # str | The report id from GET /reputation/reports
    project_id = 56 # int | Project ID
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    model = 'model_example' # str | Restrict to one analyst model (optional)
    brand = 'brand_example' # str | Restrict to one brand name, or a comma-separated list (optional)
    dimension = 'dimension_example' # str | Restrict to one reputation dimension key (optional)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # Get reputation report scores
        api_instance.get_reputation_report(id, project_id, page=page, per_page=per_page, model=model, brand=brand, dimension=dimension, output=output)
    except Exception as e:
        print("Exception when calling ReputationStudiesApi->get_reputation_report: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| The report id from GET /reputation/reports | 
 **project_id** | **int**| Project ID | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **model** | **str**| Restrict to one analyst model | [optional] 
 **brand** | **str**| Restrict to one brand name, or a comma-separated list | [optional] 
 **dimension** | **str**| Restrict to one reputation dimension key | [optional] 
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
**200** | Paginated score rows plus the report summary |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study**
> get_study(id)

Get a custom AI study

One study with its brief, the subjects it compares, the dimensions it scores them on, and its report history. Use the ids in `reports` with GET /studies/{id}/reports/{report_id}.

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
    api_instance = llmpulse.ReputationStudiesApi(api_client)
    id = 56 # int | 

    try:
        # Get a custom AI study
        api_instance.get_study(id)
    except Exception as e:
        print("Exception when calling ReputationStudiesApi->get_study: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
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
**200** | The study |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_report**
> get_study_report(id, report_id, page=page, per_page=per_page, model=model, subject=subject, dimension=dimension, output=output)

Get custom study report scores

One custom-study report's scores as flat rows: one row per analyst model, subject, dimension and attribute, with its 0-100 score and the reasoning the model gave.

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
    api_instance = llmpulse.ReputationStudiesApi(api_client)
    id = 56 # int | 
    report_id = 'report_id_example' # str | The report id from GET /studies/{id}
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    model = 'model_example' # str | Restrict to one analyst model (optional)
    subject = 'subject_example' # str | Restrict to one subject name, or a comma-separated list (optional)
    dimension = 'dimension_example' # str | Restrict to one dimension key (optional)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # Get custom study report scores
        api_instance.get_study_report(id, report_id, page=page, per_page=per_page, model=model, subject=subject, dimension=dimension, output=output)
    except Exception as e:
        print("Exception when calling ReputationStudiesApi->get_study_report: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  | 
 **report_id** | **str**| The report id from GET /studies/{id} | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **model** | **str**| Restrict to one analyst model | [optional] 
 **subject** | **str**| Restrict to one subject name, or a comma-separated list | [optional] 
 **dimension** | **str**| Restrict to one dimension key | [optional] 
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
**200** | Paginated score rows plus the report summary |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_reputation_reports**
> list_reputation_reports(project_id, page=page, per_page=per_page, output=output)

List reputation reports

The monthly multi-model analyst reports scoring the tracked brand and its competitors, newest first. Pending and failed reports are included on purpose: whether this month ran at all is often the question. Each row carries the report id, its status, and which analyst models produced data. Requires reputation monitoring to be enabled on the account.

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
    api_instance = llmpulse.ReputationStudiesApi(api_client)
    project_id = 56 # int | Project ID
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List reputation reports
        api_instance.list_reputation_reports(project_id, page=page, per_page=per_page, output=output)
    except Exception as e:
        print("Exception when calling ReputationStudiesApi->list_reputation_reports: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

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
**200** | Paginated report summaries |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_studies**
> list_studies(project_id=project_id, status=status, page=page, per_page=per_page, output=output)

List custom AI studies

The custom AI studies defined on the account: analyst reports over any set of subjects (brands, sectors, topics) and any set of dimensions. Studies belong to the ACCOUNT, not to a project, so project_id is an optional filter here and account-level studies are returned whichever project you filter by. A team member whose project access is restricted sees only the studies of the projects they can reach. Requires reputation monitoring to be enabled on the account.

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
    api_instance = llmpulse.ReputationStudiesApi(api_client)
    project_id = 56 # int | Restrict to studies attached to this project (plus account-level ones) (optional)
    status = 'status_example' # str |  (optional)
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List custom AI studies
        api_instance.list_studies(project_id=project_id, status=status, page=page, per_page=per_page, output=output)
    except Exception as e:
        print("Exception when calling ReputationStudiesApi->list_studies: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Restrict to studies attached to this project (plus account-level ones) | [optional] 
 **status** | **str**|  | [optional] 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

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
**200** | Paginated study summaries |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

