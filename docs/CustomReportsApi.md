# llmpulse.CustomReportsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_custom_report**](CustomReportsApi.md#get_custom_report) | **GET** /custom_reports/{id} | Get a custom report with its widget data
[**list_custom_reports**](CustomReportsApi.md#list_custom_reports) | **GET** /custom_reports | List custom reports
[**send_custom_report**](CustomReportsApi.md#send_custom_report) | **POST** /custom_reports/{id}/send | Send a custom report now


# **get_custom_report**
> CustomReportDetailResponse get_custom_report(project_id, id)

Get a custom report with its widget data

The configuration of one custom report (date range, filters, schedule, layout) and the data of every widget computed for today, the same numbers the report page, its shared link and its PDF show. Each widget carries its `kind` and a `data` object shaped by it: `series` for `timeseries`, `slices` for `donut`, `bars` for `bar`, `values` and `changes` for `kpi_grid`, `rows` for `table`. A widget whose data source is not connected has `available: false` and `data: null`. Nothing is saved or sent. Requires the Scale plan or above.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.custom_report_detail_response import CustomReportDetailResponse
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
    api_instance = llmpulse.CustomReportsApi(api_client)
    project_id = 56 # int | Project ID
    id = 56 # int | Custom report id, from GET /custom_reports

    try:
        # Get a custom report with its widget data
        api_response = api_instance.get_custom_report(project_id, id)
        print("The response of CustomReportsApi->get_custom_report:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CustomReportsApi->get_custom_report: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **id** | **int**| Custom report id, from GET /custom_reports | 

### Return type

[**CustomReportDetailResponse**](CustomReportDetailResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Report configuration and widget data |  -  |
**403** | Endpoint requires a higher plan tier |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_custom_reports**
> CustomReportsResponse list_custom_reports(project_id, page=page, per_page=per_page, output=output)

List custom reports

The custom reports of the project, newest first, as the Reports > Custom Reports list shows them. Recipient addresses, the shared-link token and the password are never returned. Requires the Scale plan or above.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.custom_reports_response import CustomReportsResponse
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
    api_instance = llmpulse.CustomReportsApi(api_client)
    project_id = 56 # int | Project ID
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List custom reports
        api_response = api_instance.list_custom_reports(project_id, page=page, per_page=per_page, output=output)
        print("The response of CustomReportsApi->list_custom_reports:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CustomReportsApi->list_custom_reports: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

[**CustomReportsResponse**](CustomReportsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated custom reports |  -  |
**403** | Endpoint requires a higher plan tier |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **send_custom_report**
> CustomReportSendResponse send_custom_report(id, send_custom_report_request)

Send a custom report now

Queues the report's PDF for its recipients, like the Send now button on the report page: the report must be published and have at least one recipient (ERR_INVALID_PARAM otherwise), and each report can be sent once every 10 minutes (429 ERR_RATE_LIMITED with Retry-After). Not available from a white-label portal or for a report made inside one (ERR_INTEGRATION_UNAVAILABLE). Requires the Scale plan or above, a `read_write` scope API key and, for team members, update permission on Custom Reports.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.custom_report_send_response import CustomReportSendResponse
from llmpulse.models.send_custom_report_request import SendCustomReportRequest
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
    api_instance = llmpulse.CustomReportsApi(api_client)
    id = 56 # int | Custom report id, from GET /custom_reports
    send_custom_report_request = llmpulse.SendCustomReportRequest() # SendCustomReportRequest | 

    try:
        # Send a custom report now
        api_response = api_instance.send_custom_report(id, send_custom_report_request)
        print("The response of CustomReportsApi->send_custom_report:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CustomReportsApi->send_custom_report: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Custom report id, from GET /custom_reports | 
 **send_custom_report_request** | [**SendCustomReportRequest**](SendCustomReportRequest.md)|  | 

### Return type

[**CustomReportSendResponse**](CustomReportSendResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | The report is queued for its recipients |  -  |
**403** | Writes with a read-only key answer ERR_INSUFFICIENT_SCOPE, a team member without the permission ERR_INSUFFICIENT_PERMISSION, and a request made on a white-label portal host, where the app does not offer this action, ERR_INTEGRATION_UNAVAILABLE, with the same status |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |
**429** | The report was sent less than 10 minutes ago; retry after the number of seconds in the Retry-After header |  * Retry-After - Seconds to wait before retrying <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

