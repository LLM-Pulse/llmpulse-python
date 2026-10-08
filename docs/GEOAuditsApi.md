# llmpulse.GEOAuditsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**compare_geo_audit_runs**](GEOAuditsApi.md#compare_geo_audit_runs) | **GET** /geo_audits/{id}/comparison | Compare two GEO audit runs
[**create_geo_audits**](GEOAuditsApi.md#create_geo_audits) | **POST** /geo_audits | Create GEO audits
[**delete_geo_audit**](GEOAuditsApi.md#delete_geo_audit) | **DELETE** /geo_audits/{id} | Delete (archive) a GEO audit
[**get_geo_audit**](GEOAuditsApi.md#get_geo_audit) | **GET** /geo_audits/{id} | Get a GEO audit
[**get_geo_audit_run**](GEOAuditsApi.md#get_geo_audit_run) | **GET** /geo_audits/{geo_audit_id}/runs/{sequence} | Get a GEO audit run
[**list_geo_alerts**](GEOAuditsApi.md#list_geo_alerts) | **GET** /geo_alerts | List GEO audit alerts
[**list_geo_audit_findings**](GEOAuditsApi.md#list_geo_audit_findings) | **GET** /geo_audits/{geo_audit_id}/runs/{sequence}/findings | List the findings of a GEO audit run
[**list_geo_audit_issues**](GEOAuditsApi.md#list_geo_audit_issues) | **GET** /geo_audits/{geo_audit_id}/issues | List the issues of a GEO audit
[**list_geo_audit_runs**](GEOAuditsApi.md#list_geo_audit_runs) | **GET** /geo_audits/{geo_audit_id}/runs | List the runs of a GEO audit
[**list_geo_audits**](GEOAuditsApi.md#list_geo_audits) | **GET** /geo_audits | List GEO audits
[**run_geo_audit**](GEOAuditsApi.md#run_geo_audit) | **POST** /geo_audits/{geo_audit_id}/runs | Run a GEO audit now
[**update_geo_audit**](GEOAuditsApi.md#update_geo_audit) | **PATCH** /geo_audits/{id} | Update a GEO audit
[**update_geo_audit_issue**](GEOAuditsApi.md#update_geo_audit_issue) | **PATCH** /geo_audits/{geo_audit_id}/issues/{id} | Accept or reopen a GEO audit issue


# **compare_geo_audit_runs**
> GeoAuditComparison compare_geo_audit_runs(project_id, id, from_run=from_run, to_run=to_run)

Compare two GEO audit runs

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_audit_comparison import GeoAuditComparison
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    project_id = 56 # int | Project ID
    id = 'id_example' # str | Audit id
    from_run = 56 # int | Run number to compare from (default the run before to_run) (optional)
    to_run = 56 # int | Run number to compare to (default the latest completed run) (optional)

    try:
        # Compare two GEO audit runs
        api_response = api_instance.compare_geo_audit_runs(project_id, id, from_run=from_run, to_run=to_run)
        print("The response of GEOAuditsApi->compare_geo_audit_runs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->compare_geo_audit_runs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **id** | **str**| Audit id | 
 **from_run** | **int**| Run number to compare from (default the run before to_run) | [optional] 
 **to_run** | **int**| Run number to compare to (default the latest completed run) | [optional] 

### Return type

[**GeoAuditComparison**](GeoAuditComparison.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The comparison |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_geo_audits**
> GeoAuditCreateResponse create_geo_audits(geo_audit_create_request)

Create GEO audits

Creates one audit per entry of audit_types and starts the first run of each (it counts against the manual run limits: 6 per audit per hour, 200 per account per day). cadence weekly or monthly is accepted only for types whose checks are tracked run to run, and counts against the plan limit of active recurring audits (ERR_LIMIT_REACHED). Creating an audit that was archived restores it with its history. Requires a `read_write` scope API key.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_audit_create_request import GeoAuditCreateRequest
from llmpulse.models.geo_audit_create_response import GeoAuditCreateResponse
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    geo_audit_create_request = llmpulse.GeoAuditCreateRequest() # GeoAuditCreateRequest | 

    try:
        # Create GEO audits
        api_response = api_instance.create_geo_audits(geo_audit_create_request)
        print("The response of GEOAuditsApi->create_geo_audits:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->create_geo_audits: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **geo_audit_create_request** | [**GeoAuditCreateRequest**](GeoAuditCreateRequest.md)|  | 

### Return type

[**GeoAuditCreateResponse**](GeoAuditCreateResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The created audits |  -  |
**403** | API key lacks write permission |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_geo_audit**
> GeoAuditArchived delete_geo_audit(project_id, id)

Delete (archive) a GEO audit

Archives the audit. Requires a `read_write` scope API key and, for team members, delete permission on GEO Optimization.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_audit_archived import GeoAuditArchived
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    project_id = 56 # int | Project ID
    id = 'id_example' # str | Audit id

    try:
        # Delete (archive) a GEO audit
        api_response = api_instance.delete_geo_audit(project_id, id)
        print("The response of GEOAuditsApi->delete_geo_audit:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->delete_geo_audit: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **id** | **str**| Audit id | 

### Return type

[**GeoAuditArchived**](GeoAuditArchived.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Archived |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_geo_audit**
> GeoAuditResponse get_geo_audit(project_id, id)

Get a GEO audit

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_audit_response import GeoAuditResponse
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    project_id = 56 # int | Project ID
    id = 'id_example' # str | Audit id

    try:
        # Get a GEO audit
        api_response = api_instance.get_geo_audit(project_id, id)
        print("The response of GEOAuditsApi->get_geo_audit:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->get_geo_audit: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **id** | **str**| Audit id | 

### Return type

[**GeoAuditResponse**](GeoAuditResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The audit |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_geo_audit_run**
> GeoAuditRunDetail get_geo_audit_run(project_id, geo_audit_id, sequence)

Get a GEO audit run

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_audit_run_detail import GeoAuditRunDetail
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    project_id = 56 # int | Project ID
    geo_audit_id = 'geo_audit_id_example' # str | Audit id
    sequence = 56 # int | Run number within the audit

    try:
        # Get a GEO audit run
        api_response = api_instance.get_geo_audit_run(project_id, geo_audit_id, sequence)
        print("The response of GEOAuditsApi->get_geo_audit_run:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->get_geo_audit_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **geo_audit_id** | **str**| Audit id | 
 **sequence** | **int**| Run number within the audit | 

### Return type

[**GeoAuditRunDetail**](GeoAuditRunDetail.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The run with its result |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_geo_alerts**
> GeoAlertList list_geo_alerts(project_id, audit_id=audit_id, page=page, per_page=per_page)

List GEO audit alerts

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_alert_list import GeoAlertList
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    project_id = 56 # int | Project ID
    audit_id = 'audit_id_example' # str | Only alerts of this audit (optional)
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)

    try:
        # List GEO audit alerts
        api_response = api_instance.list_geo_alerts(project_id, audit_id=audit_id, page=page, per_page=per_page)
        print("The response of GEOAuditsApi->list_geo_alerts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->list_geo_alerts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **audit_id** | **str**| Only alerts of this audit | [optional] 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]

### Return type

[**GeoAlertList**](GeoAlertList.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated alerts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_geo_audit_findings**
> GeoAuditFindingList list_geo_audit_findings(project_id, geo_audit_id, sequence, page=page, per_page=per_page, output=output)

List the findings of a GEO audit run

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_audit_finding_list import GeoAuditFindingList
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    project_id = 56 # int | Project ID
    geo_audit_id = 'geo_audit_id_example' # str | Audit id
    sequence = 56 # int | Run number within the audit
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List the findings of a GEO audit run
        api_response = api_instance.list_geo_audit_findings(project_id, geo_audit_id, sequence, page=page, per_page=per_page, output=output)
        print("The response of GEOAuditsApi->list_geo_audit_findings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->list_geo_audit_findings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **geo_audit_id** | **str**| Audit id | 
 **sequence** | **int**| Run number within the audit | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

[**GeoAuditFindingList**](GeoAuditFindingList.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated findings |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_geo_audit_issues**
> GeoAuditIssueList list_geo_audit_issues(project_id, geo_audit_id, state=state, page=page, per_page=per_page)

List the issues of a GEO audit

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_audit_issue_list import GeoAuditIssueList
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    project_id = 56 # int | Project ID
    geo_audit_id = 'geo_audit_id_example' # str | Audit id
    state = 'state_example' # str | open means open and not accepted; default all (optional)
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)

    try:
        # List the issues of a GEO audit
        api_response = api_instance.list_geo_audit_issues(project_id, geo_audit_id, state=state, page=page, per_page=per_page)
        print("The response of GEOAuditsApi->list_geo_audit_issues:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->list_geo_audit_issues: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **geo_audit_id** | **str**| Audit id | 
 **state** | **str**| open means open and not accepted; default all | [optional] 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]

### Return type

[**GeoAuditIssueList**](GeoAuditIssueList.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated issues |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_geo_audit_runs**
> GeoAuditRunList list_geo_audit_runs(project_id, geo_audit_id, page=page, per_page=per_page, output=output)

List the runs of a GEO audit

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_audit_run_list import GeoAuditRunList
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    project_id = 56 # int | Project ID
    geo_audit_id = 'geo_audit_id_example' # str | Audit id
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List the runs of a GEO audit
        api_response = api_instance.list_geo_audit_runs(project_id, geo_audit_id, page=page, per_page=per_page, output=output)
        print("The response of GEOAuditsApi->list_geo_audit_runs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->list_geo_audit_runs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **geo_audit_id** | **str**| Audit id | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

[**GeoAuditRunList**](GeoAuditRunList.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated runs |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_geo_audits**
> GeoAuditList list_geo_audits(project_id, audit_type=audit_type, status=status, cadence=cadence, page=page, per_page=per_page)

List GEO audits

Lists the project's audits, most recently updated first. Archived audits are left out unless status=archived.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_audit_list import GeoAuditList
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    project_id = 56 # int | Project ID
    audit_type = 'audit_type_example' # str |  (optional)
    status = 'status_example' # str |  (optional)
    cadence = 'cadence_example' # str |  (optional)
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)

    try:
        # List GEO audits
        api_response = api_instance.list_geo_audits(project_id, audit_type=audit_type, status=status, cadence=cadence, page=page, per_page=per_page)
        print("The response of GEOAuditsApi->list_geo_audits:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->list_geo_audits: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **audit_type** | **str**|  | [optional] 
 **status** | **str**|  | [optional] 
 **cadence** | **str**|  | [optional] 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]

### Return type

[**GeoAuditList**](GeoAuditList.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated audits |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **run_geo_audit**
> GeoAuditRunResponse run_geo_audit(project_id, geo_audit_id)

Run a GEO audit now

Starts a run and returns it with status queued; poll GET /geo_audits/{geo_audit_id}/runs/{sequence} until status is completed, failed or unreachable. Limited to 6 manual runs per audit per rolling hour and 200 per account per day (ERR_LIMIT_REACHED); scheduled runs do not count. Requires a `read_write` scope API key.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_audit_run_response import GeoAuditRunResponse
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    project_id = 56 # int | Project ID
    geo_audit_id = 'geo_audit_id_example' # str | Audit id

    try:
        # Run a GEO audit now
        api_response = api_instance.run_geo_audit(project_id, geo_audit_id)
        print("The response of GEOAuditsApi->run_geo_audit:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->run_geo_audit: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **geo_audit_id** | **str**| Audit id | 

### Return type

[**GeoAuditRunResponse**](GeoAuditRunResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The new run |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_geo_audit**
> GeoAuditResponse update_geo_audit(id, geo_audit_update_request)

Update a GEO audit

Updates the schedule, the email alerts or the status. Making an audit recurring or resuming it counts against the plan limit of active recurring audits (ERR_LIMIT_REACHED). Requires a `read_write` scope API key and, for team members, update permission on GEO Optimization.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_audit_response import GeoAuditResponse
from llmpulse.models.geo_audit_update_request import GeoAuditUpdateRequest
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    id = 'id_example' # str | Audit id
    geo_audit_update_request = llmpulse.GeoAuditUpdateRequest() # GeoAuditUpdateRequest | 

    try:
        # Update a GEO audit
        api_response = api_instance.update_geo_audit(id, geo_audit_update_request)
        print("The response of GEOAuditsApi->update_geo_audit:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->update_geo_audit: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Audit id | 
 **geo_audit_update_request** | [**GeoAuditUpdateRequest**](GeoAuditUpdateRequest.md)|  | 

### Return type

[**GeoAuditResponse**](GeoAuditResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated audit |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_geo_audit_issue**
> GeoAuditIssueResponse update_geo_audit_issue(geo_audit_id, id, geo_audit_issue_update_request)

Accept or reopen a GEO audit issue

Requires a `read_write` scope API key and, for team members, update permission on GEO Optimization.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.geo_audit_issue_response import GeoAuditIssueResponse
from llmpulse.models.geo_audit_issue_update_request import GeoAuditIssueUpdateRequest
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
    api_instance = llmpulse.GEOAuditsApi(api_client)
    geo_audit_id = 'geo_audit_id_example' # str | Audit id
    id = 56 # int | Issue id
    geo_audit_issue_update_request = llmpulse.GeoAuditIssueUpdateRequest() # GeoAuditIssueUpdateRequest | 

    try:
        # Accept or reopen a GEO audit issue
        api_response = api_instance.update_geo_audit_issue(geo_audit_id, id, geo_audit_issue_update_request)
        print("The response of GEOAuditsApi->update_geo_audit_issue:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GEOAuditsApi->update_geo_audit_issue: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **geo_audit_id** | **str**| Audit id | 
 **id** | **int**| Issue id | 
 **geo_audit_issue_update_request** | [**GeoAuditIssueUpdateRequest**](GeoAuditIssueUpdateRequest.md)|  | 

### Return type

[**GeoAuditIssueResponse**](GeoAuditIssueResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated issue |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

