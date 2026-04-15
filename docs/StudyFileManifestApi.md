# immport_client.StudyFileManifestApi

All URIs are relative to *https://immport.org/data/query*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_file_details**](StudyFileManifestApi.md#get_file_details) | **GET** /api/study/manifest/{studyAccession} | Retrieve file manifest with DRS ID&#39;s for a study


# **get_file_details**
> List[FileDetails] get_file_details(study_accession, file_type=file_type, format=format)

Retrieve file manifest with DRS ID's for a study

Returns file manifest that contains DRS Id's(fileUUID), checksum, file size,path, file name. This endpoint can be used in conjunction with enpoint: /drs/download/{accessMethod}/{fileUUID}

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.file_details import FileDetails
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
    api_instance = immport_client.StudyFileManifestApi(api_client)
    study_accession = 'SDY1' # str | Study Accession
    file_type = 'all' # str | File Type: all(default), archive_file, release_file, study_file, protocol_file, result_file (optional) (default to 'all')
    format = 'json' # str | Format: json(default), tsv (optional) (default to 'json')

    try:
        # Retrieve file manifest with DRS ID's for a study
        api_response = api_instance.get_file_details(study_accession, file_type=file_type, format=format)
        print("The response of StudyFileManifestApi->get_file_details:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyFileManifestApi->get_file_details: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**| Study Accession | 
 **file_type** | **str**| File Type: all(default), archive_file, release_file, study_file, protocol_file, result_file | [optional] [default to &#39;all&#39;]
 **format** | **str**| Format: json(default), tsv | [optional] [default to &#39;json&#39;]

### Return type

[**List[FileDetails]**](FileDetails.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Manifest data |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

