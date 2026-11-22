# llmpulse.BingWebmasterToolsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_bing_webmaster_pages**](BingWebmasterToolsApi.md#get_bing_webmaster_pages) | **GET** /bing_webmaster/pages | Top Bing Webmaster Tools pages (Growth+)
[**get_bing_webmaster_queries**](BingWebmasterToolsApi.md#get_bing_webmaster_queries) | **GET** /bing_webmaster/queries | Top Bing Webmaster Tools queries (Growth+)
[**get_bing_webmaster_summary**](BingWebmasterToolsApi.md#get_bing_webmaster_summary) | **GET** /bing_webmaster/summary | Bing Webmaster Tools summary (Growth+)
[**get_bing_webmaster_timeseries**](BingWebmasterToolsApi.md#get_bing_webmaster_timeseries) | **GET** /bing_webmaster/timeseries | Bing Webmaster Tools time series (Growth+)


# **get_bing_webmaster_pages**
> BingWebmasterListResponse get_bing_webmaster_pages(project_id, range=range, var_from=var_from, to=to, sort=sort, page=page, per_page=per_page, output=output)

Top Bing Webmaster Tools pages (Growth+)

The landing pages of the project's connected Bing Webmaster Tools site in Bing Search, ranked and paginated. Each row sums the weekly figures Bing reports for the weeks whose week_ending (the Friday that closes a Bing week) falls in the window: clicks, impressions, ctr (a 0..1 fraction), avg_impression_position weighted by impressions and avg_click_position weighted by clicks (null without clicks). Bing reports only its top pages of each week, about 100, so the rows are not a complete set and never add up to /bing_webmaster/summary. weeks_covered counts the weeks found in the window and data_through is the last week_ending synced. history_current is false right after the site was changed and before its first sync: data is then empty. Requires a connected Bing Webmaster Tools site (ERR_BING_WEBMASTER_NOT_CONNECTED) and the Growth plan or above.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.bing_webmaster_list_response import BingWebmasterListResponse
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
    api_instance = llmpulse.BingWebmasterToolsApi(api_client)
    project_id = 56 # int | Project ID
    range = 56 # int | Number of days to look back, today included (alternative to from/to, which win when both are given). At most 487, the window the Search Console endpoints accept; about 13 months of Bing data are kept. A value that is not a plain positive number returns 422 ERR_INVALID_PARAM even beside from/to. (optional)
    var_from = '2013-10-20' # date | Start date (YYYY-MM-DD). Without from and to, the window is the last 30 days, today included; with only to, from is 30 days before today. (optional)
    to = '2013-10-20' # date | End date (YYYY-MM-DD), inclusive. Defaults to today. data_through in the response says how far the synced data reaches. (optional)
    sort = 'impressions' # str | Sort key. impressions, clicks and ctr sort descending, the two positions ascending; rows without a value sort last. (optional) (default to 'impressions')
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # Top Bing Webmaster Tools pages (Growth+)
        api_response = api_instance.get_bing_webmaster_pages(project_id, range=range, var_from=var_from, to=to, sort=sort, page=page, per_page=per_page, output=output)
        print("The response of BingWebmasterToolsApi->get_bing_webmaster_pages:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BingWebmasterToolsApi->get_bing_webmaster_pages: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **range** | **int**| Number of days to look back, today included (alternative to from/to, which win when both are given). At most 487, the window the Search Console endpoints accept; about 13 months of Bing data are kept. A value that is not a plain positive number returns 422 ERR_INVALID_PARAM even beside from/to. | [optional] 
 **var_from** | **date**| Start date (YYYY-MM-DD). Without from and to, the window is the last 30 days, today included; with only to, from is 30 days before today. | [optional] 
 **to** | **date**| End date (YYYY-MM-DD), inclusive. Defaults to today. data_through in the response says how far the synced data reaches. | [optional] 
 **sort** | **str**| Sort key. impressions, clicks and ctr sort descending, the two positions ascending; rows without a value sort last. | [optional] [default to &#39;impressions&#39;]
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

[**BingWebmasterListResponse**](BingWebmasterListResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Top pages |  -  |
**401** | Authentication failed |  -  |
**403** | Endpoint requires the Growth plan or above |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_bing_webmaster_queries**
> BingWebmasterListResponse get_bing_webmaster_queries(project_id, range=range, var_from=var_from, to=to, sort=sort, page=page, per_page=per_page, output=output)

Top Bing Webmaster Tools queries (Growth+)

The Bing search queries of the project's connected Bing Webmaster Tools site, ranked and paginated. Each row sums the weekly figures Bing reports for the weeks whose week_ending (the Friday that closes a Bing week) falls in the window: clicks, impressions, ctr (a 0..1 fraction), avg_impression_position weighted by impressions and avg_click_position weighted by clicks (null without clicks). Bing reports only its top queries of each week, about 100, so the rows are not a complete set and never add up to /bing_webmaster/summary. weeks_covered counts the weeks found in the window and data_through is the last week_ending synced. history_current is false right after the site was changed and before its first sync: data is then empty. Requires a connected Bing Webmaster Tools site (ERR_BING_WEBMASTER_NOT_CONNECTED) and the Growth plan or above.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.bing_webmaster_list_response import BingWebmasterListResponse
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
    api_instance = llmpulse.BingWebmasterToolsApi(api_client)
    project_id = 56 # int | Project ID
    range = 56 # int | Number of days to look back, today included (alternative to from/to, which win when both are given). At most 487, the window the Search Console endpoints accept; about 13 months of Bing data are kept. A value that is not a plain positive number returns 422 ERR_INVALID_PARAM even beside from/to. (optional)
    var_from = '2013-10-20' # date | Start date (YYYY-MM-DD). Without from and to, the window is the last 30 days, today included; with only to, from is 30 days before today. (optional)
    to = '2013-10-20' # date | End date (YYYY-MM-DD), inclusive. Defaults to today. data_through in the response says how far the synced data reaches. (optional)
    sort = 'impressions' # str | Sort key. impressions, clicks and ctr sort descending, the two positions ascending; rows without a value sort last. (optional) (default to 'impressions')
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # Top Bing Webmaster Tools queries (Growth+)
        api_response = api_instance.get_bing_webmaster_queries(project_id, range=range, var_from=var_from, to=to, sort=sort, page=page, per_page=per_page, output=output)
        print("The response of BingWebmasterToolsApi->get_bing_webmaster_queries:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BingWebmasterToolsApi->get_bing_webmaster_queries: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **range** | **int**| Number of days to look back, today included (alternative to from/to, which win when both are given). At most 487, the window the Search Console endpoints accept; about 13 months of Bing data are kept. A value that is not a plain positive number returns 422 ERR_INVALID_PARAM even beside from/to. | [optional] 
 **var_from** | **date**| Start date (YYYY-MM-DD). Without from and to, the window is the last 30 days, today included; with only to, from is 30 days before today. | [optional] 
 **to** | **date**| End date (YYYY-MM-DD), inclusive. Defaults to today. data_through in the response says how far the synced data reaches. | [optional] 
 **sort** | **str**| Sort key. impressions, clicks and ctr sort descending, the two positions ascending; rows without a value sort last. | [optional] [default to &#39;impressions&#39;]
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

[**BingWebmasterListResponse**](BingWebmasterListResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Top queries |  -  |
**401** | Authentication failed |  -  |
**403** | Endpoint requires the Growth plan or above |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_bing_webmaster_summary**
> BingWebmasterSummaryResponse get_bing_webmaster_summary(project_id, range=range, var_from=var_from, to=to)

Bing Webmaster Tools summary (Growth+)

Bing Search clicks, impressions and ctr (a 0..1 fraction) of the project's connected Bing Webmaster Tools site over a date range, summed from the daily site totals synced once a day. Bing reports no average position in its daily totals. About 13 months of history are kept; data_through is the last day synced, and later days are missing, not zero. history_current is false right after the site was changed in Preferences > Project Settings > Connections and before its first sync: the totals are then zero and data_through and last_synced_at null. A connection whose sync_status is on_hold (Bing refused the stored API key, or the site is no longer verified) still answers from the data already synced. Requires a connected Bing Webmaster Tools site and the Growth plan or above; otherwise returns ERR_BING_WEBMASTER_NOT_CONNECTED (with meta.connect_url) or ERR_PLAN_REQUIRED.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.bing_webmaster_summary_response import BingWebmasterSummaryResponse
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
    api_instance = llmpulse.BingWebmasterToolsApi(api_client)
    project_id = 56 # int | Project ID
    range = 56 # int | Number of days to look back, today included (alternative to from/to, which win when both are given). At most 487, the window the Search Console endpoints accept; about 13 months of Bing data are kept. A value that is not a plain positive number returns 422 ERR_INVALID_PARAM even beside from/to. (optional)
    var_from = '2013-10-20' # date | Start date (YYYY-MM-DD). Without from and to, the window is the last 30 days, today included; with only to, from is 30 days before today. (optional)
    to = '2013-10-20' # date | End date (YYYY-MM-DD), inclusive. Defaults to today. data_through in the response says how far the synced data reaches. (optional)

    try:
        # Bing Webmaster Tools summary (Growth+)
        api_response = api_instance.get_bing_webmaster_summary(project_id, range=range, var_from=var_from, to=to)
        print("The response of BingWebmasterToolsApi->get_bing_webmaster_summary:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BingWebmasterToolsApi->get_bing_webmaster_summary: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **range** | **int**| Number of days to look back, today included (alternative to from/to, which win when both are given). At most 487, the window the Search Console endpoints accept; about 13 months of Bing data are kept. A value that is not a plain positive number returns 422 ERR_INVALID_PARAM even beside from/to. | [optional] 
 **var_from** | **date**| Start date (YYYY-MM-DD). Without from and to, the window is the last 30 days, today included; with only to, from is 30 days before today. | [optional] 
 **to** | **date**| End date (YYYY-MM-DD), inclusive. Defaults to today. data_through in the response says how far the synced data reaches. | [optional] 

### Return type

[**BingWebmasterSummaryResponse**](BingWebmasterSummaryResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Bing Webmaster Tools summary |  -  |
**401** | Authentication failed |  -  |
**403** | Endpoint requires the Growth plan or above |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_bing_webmaster_timeseries**
> BingWebmasterTimeseriesResponse get_bing_webmaster_timeseries(project_id, range=range, var_from=var_from, to=to, granularity=granularity, output=output)

Bing Webmaster Tools time series (Growth+)

Bing Search clicks, impressions and ctr (a 0..1 fraction) of the project's connected Bing Webmaster Tools site, bucketed by day, week (starting Monday) or month from the daily site totals synced once a day. Days without synced data are left out of the series, not reported as zero. Bing reports no average position in its daily totals. About 13 months of history are kept. history_current is false right after the site was changed and before its first sync: data is then empty. Requires a connected Bing Webmaster Tools site (ERR_BING_WEBMASTER_NOT_CONNECTED) and the Growth plan or above.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.bing_webmaster_timeseries_response import BingWebmasterTimeseriesResponse
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
    api_instance = llmpulse.BingWebmasterToolsApi(api_client)
    project_id = 56 # int | Project ID
    range = 56 # int | Number of days to look back, today included (alternative to from/to, which win when both are given). At most 487, the window the Search Console endpoints accept; about 13 months of Bing data are kept. A value that is not a plain positive number returns 422 ERR_INVALID_PARAM even beside from/to. (optional)
    var_from = '2013-10-20' # date | Start date (YYYY-MM-DD). Without from and to, the window is the last 30 days, today included; with only to, from is 30 days before today. (optional)
    to = '2013-10-20' # date | End date (YYYY-MM-DD), inclusive. Defaults to today. data_through in the response says how far the synced data reaches. (optional)
    granularity = 'granularity_example' # str |  (optional)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # Bing Webmaster Tools time series (Growth+)
        api_response = api_instance.get_bing_webmaster_timeseries(project_id, range=range, var_from=var_from, to=to, granularity=granularity, output=output)
        print("The response of BingWebmasterToolsApi->get_bing_webmaster_timeseries:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BingWebmasterToolsApi->get_bing_webmaster_timeseries: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **range** | **int**| Number of days to look back, today included (alternative to from/to, which win when both are given). At most 487, the window the Search Console endpoints accept; about 13 months of Bing data are kept. A value that is not a plain positive number returns 422 ERR_INVALID_PARAM even beside from/to. | [optional] 
 **var_from** | **date**| Start date (YYYY-MM-DD). Without from and to, the window is the last 30 days, today included; with only to, from is 30 days before today. | [optional] 
 **to** | **date**| End date (YYYY-MM-DD), inclusive. Defaults to today. data_through in the response says how far the synced data reaches. | [optional] 
 **granularity** | **str**|  | [optional] 
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

[**BingWebmasterTimeseriesResponse**](BingWebmasterTimeseriesResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Bing Webmaster Tools time series |  -  |
**401** | Authentication failed |  -  |
**403** | Endpoint requires the Growth plan or above |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

