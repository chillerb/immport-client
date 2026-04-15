# immport_client.DownloadStudyFilesApi

All URIs are relative to *https://immport.org/data/query*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_url_from_drs**](DownloadStudyFilesApi.md#get_url_from_drs) | **GET** /drs/download/{accessMethod}/{fileUUID} | Get download URL using DRS ID


# **get_url_from_drs**
> FileDownloadURL get_url_from_drs(file_uuid, access_method)

Get download URL using DRS ID

Returns a signed S3 URL or stream URL for the given DRS file UUID and access method.

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.file_download_url import FileDownloadURL
from immport_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://immport.org/data/query
# See configuration.py for a list of all supported configuration parameters.
configuration = immport_client.Configuration(
    host = "https://immport.org/data/query"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

configuration.access_token = os.environ["ACCESS_TOKEN"]

# Enter a context with an instance of the API client
with immport_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = immport_client.DownloadStudyFilesApi(api_client)
    file_uuid = '81944983-0aaf-4b55-a1ef-e2681c8b258b' # str | DRS file UUID
    access_method = 's3' # str | Access method to retrieve the file: s3 or stream

    try:
        # Get download URL using DRS ID
        api_response = api_instance.get_url_from_drs(file_uuid, access_method)
        print("The response of DownloadStudyFilesApi->get_url_from_drs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DownloadStudyFilesApi->get_url_from_drs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_uuid** | **str**| DRS file UUID | 
 **access_method** | **str**| Access method to retrieve the file: s3 or stream | 

### Return type

[**FileDownloadURL**](FileDownloadURL.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**400** | Bad Request |  -  |
**500** | Internal server error |  -  |
**401** | Unauthorized |  -  |
**200** | Download URL (signed s3 or stream) returned successfully |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

