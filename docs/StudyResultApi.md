# immport_client.StudyResultApi

All URIs are relative to *https://immport.org/data/query*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_elisa_result**](StudyResultApi.md#get_elisa_result) | **GET** /result/elisa | Retrieve ELISA results using filters
[**get_elispot_result**](StudyResultApi.md#get_elispot_result) | **GET** /result/elispot | Retrieve Elispot results using filters
[**get_fcs_analyzed_result**](StudyResultApi.md#get_fcs_analyzed_result) | **GET** /result/fcsAnalyzed | Retrieve FcsAnalyzed results using filters
[**get_file_path**](StudyResultApi.md#get_file_path) | **GET** /result/filePath | Retrieve File Paths using filters
[**get_hai_result**](StudyResultApi.md#get_hai_result) | **GET** /result/hai | Retrieve HAI results using filters
[**get_hla_typing_result**](StudyResultApi.md#get_hla_typing_result) | **GET** /result/hlaTyping | Retrieve HLA Typing results using filters
[**get_kir_typing_result**](StudyResultApi.md#get_kir_typing_result) | **GET** /result/kirTyping | Retrieve kIR Typing results using filters
[**get_mass_spectrometry_result**](StudyResultApi.md#get_mass_spectrometry_result) | **GET** /result/massSpectrometryResult | Retrieve Mass Spectrometry results using filters
[**get_mbaa_result**](StudyResultApi.md#get_mbaa_result) | **GET** /result/mbaa | Retrieve MBAA results using filters
[**get_neut_ab_titer_result**](StudyResultApi.md#get_neut_ab_titer_result) | **GET** /result/neutAbTiter | Retrieve Neutralizing Antibody Titer results using filters
[**get_pcr_result**](StudyResultApi.md#get_pcr_result) | **GET** /result/pcr | Retrieve PCR results using filters


# **get_elisa_result**
> List[VElisaResult] get_elisa_result(filter_criteria_fields)

Retrieve ELISA results using filters

Returns ELISA results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.filter_criteria_fields import FilterCriteriaFields
from immport_client.models.v_elisa_result import VElisaResult
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
    api_instance = immport_client.StudyResultApi(api_client)
    filter_criteria_fields = immport_client.FilterCriteriaFields() # FilterCriteriaFields | 

    try:
        # Retrieve ELISA results using filters
        api_response = api_instance.get_elisa_result(filter_criteria_fields)
        print("The response of StudyResultApi->get_elisa_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_elisa_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_criteria_fields** | [**FilterCriteriaFields**](.md)|  | 

### Return type

[**List[VElisaResult]**](VElisaResult.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Elisa Results |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_elispot_result**
> List[VElispotResult] get_elispot_result(filter_criteria_fields)

Retrieve Elispot results using filters

Returns Elispot results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.filter_criteria_fields import FilterCriteriaFields
from immport_client.models.v_elispot_result import VElispotResult
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
    api_instance = immport_client.StudyResultApi(api_client)
    filter_criteria_fields = immport_client.FilterCriteriaFields() # FilterCriteriaFields | 

    try:
        # Retrieve Elispot results using filters
        api_response = api_instance.get_elispot_result(filter_criteria_fields)
        print("The response of StudyResultApi->get_elispot_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_elispot_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_criteria_fields** | [**FilterCriteriaFields**](.md)|  | 

### Return type

[**List[VElispotResult]**](VElispotResult.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Elispot Results |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_fcs_analyzed_result**
> List[VFcsAnalyzedResult] get_fcs_analyzed_result(filter_criteria_fields)

Retrieve FcsAnalyzed results using filters

Returns FcsAnalyzed results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.filter_criteria_fields import FilterCriteriaFields
from immport_client.models.v_fcs_analyzed_result import VFcsAnalyzedResult
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
    api_instance = immport_client.StudyResultApi(api_client)
    filter_criteria_fields = immport_client.FilterCriteriaFields() # FilterCriteriaFields | 

    try:
        # Retrieve FcsAnalyzed results using filters
        api_response = api_instance.get_fcs_analyzed_result(filter_criteria_fields)
        print("The response of StudyResultApi->get_fcs_analyzed_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_fcs_analyzed_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_criteria_fields** | [**FilterCriteriaFields**](.md)|  | 

### Return type

[**List[VFcsAnalyzedResult]**](VFcsAnalyzedResult.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return FcsAnalyzed Results |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_file_path**
> List[VResultFilePath] get_file_path(filter_criteria_fields)

Retrieve File Paths using filters

Returns File Paths based on filter criteria
These paths represent file locations within the ImmPort SharedData File system.
Review the File Download tutorial to see how to use these Paths to retrieve the file.

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.filter_criteria_fields import FilterCriteriaFields
from immport_client.models.v_result_file_path import VResultFilePath
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
    api_instance = immport_client.StudyResultApi(api_client)
    filter_criteria_fields = immport_client.FilterCriteriaFields() # FilterCriteriaFields | 

    try:
        # Retrieve File Paths using filters
        api_response = api_instance.get_file_path(filter_criteria_fields)
        print("The response of StudyResultApi->get_file_path:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_file_path: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_criteria_fields** | [**FilterCriteriaFields**](.md)|  | 

### Return type

[**List[VResultFilePath]**](VResultFilePath.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return File Paths |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_hai_result**
> List[VHaiResult] get_hai_result(filter_criteria_fields)

Retrieve HAI results using filters

Returns HAI results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.filter_criteria_fields import FilterCriteriaFields
from immport_client.models.v_hai_result import VHaiResult
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
    api_instance = immport_client.StudyResultApi(api_client)
    filter_criteria_fields = immport_client.FilterCriteriaFields() # FilterCriteriaFields | 

    try:
        # Retrieve HAI results using filters
        api_response = api_instance.get_hai_result(filter_criteria_fields)
        print("The response of StudyResultApi->get_hai_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_hai_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_criteria_fields** | [**FilterCriteriaFields**](.md)|  | 

### Return type

[**List[VHaiResult]**](VHaiResult.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return HAI Results |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_hla_typing_result**
> List[VHlaTypingResult] get_hla_typing_result(filter_criteria_fields)

Retrieve HLA Typing results using filters

Returns HLA Typing results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.filter_criteria_fields import FilterCriteriaFields
from immport_client.models.v_hla_typing_result import VHlaTypingResult
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
    api_instance = immport_client.StudyResultApi(api_client)
    filter_criteria_fields = immport_client.FilterCriteriaFields() # FilterCriteriaFields | 

    try:
        # Retrieve HLA Typing results using filters
        api_response = api_instance.get_hla_typing_result(filter_criteria_fields)
        print("The response of StudyResultApi->get_hla_typing_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_hla_typing_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_criteria_fields** | [**FilterCriteriaFields**](.md)|  | 

### Return type

[**List[VHlaTypingResult]**](VHlaTypingResult.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return HLA Typing Results |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_kir_typing_result**
> List[VKirTypingResult] get_kir_typing_result(filter_criteria_fields)

Retrieve kIR Typing results using filters

Returns KIR Typing results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.filter_criteria_fields import FilterCriteriaFields
from immport_client.models.v_kir_typing_result import VKirTypingResult
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
    api_instance = immport_client.StudyResultApi(api_client)
    filter_criteria_fields = immport_client.FilterCriteriaFields() # FilterCriteriaFields | 

    try:
        # Retrieve kIR Typing results using filters
        api_response = api_instance.get_kir_typing_result(filter_criteria_fields)
        print("The response of StudyResultApi->get_kir_typing_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_kir_typing_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_criteria_fields** | [**FilterCriteriaFields**](.md)|  | 

### Return type

[**List[VKirTypingResult]**](VKirTypingResult.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return KIR Typing Results |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_mass_spectrometry_result**
> List[MassSpectrometryResult] get_mass_spectrometry_result(filter_criteria_fields)

Retrieve Mass Spectrometry results using filters

Returns Mass Spectrometry results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.filter_criteria_fields import FilterCriteriaFields
from immport_client.models.mass_spectrometry_result import MassSpectrometryResult
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
    api_instance = immport_client.StudyResultApi(api_client)
    filter_criteria_fields = immport_client.FilterCriteriaFields() # FilterCriteriaFields | 

    try:
        # Retrieve Mass Spectrometry results using filters
        api_response = api_instance.get_mass_spectrometry_result(filter_criteria_fields)
        print("The response of StudyResultApi->get_mass_spectrometry_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_mass_spectrometry_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_criteria_fields** | [**FilterCriteriaFields**](.md)|  | 

### Return type

[**List[MassSpectrometryResult]**](MassSpectrometryResult.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Mass Spectrometry Results |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_mbaa_result**
> List[VMbaaResult] get_mbaa_result(filter_criteria_fields)

Retrieve MBAA results using filters

Returns MBAA results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.filter_criteria_fields import FilterCriteriaFields
from immport_client.models.v_mbaa_result import VMbaaResult
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
    api_instance = immport_client.StudyResultApi(api_client)
    filter_criteria_fields = immport_client.FilterCriteriaFields() # FilterCriteriaFields | 

    try:
        # Retrieve MBAA results using filters
        api_response = api_instance.get_mbaa_result(filter_criteria_fields)
        print("The response of StudyResultApi->get_mbaa_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_mbaa_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_criteria_fields** | [**FilterCriteriaFields**](.md)|  | 

### Return type

[**List[VMbaaResult]**](VMbaaResult.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return MBAA Typing Results |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_neut_ab_titer_result**
> List[VNeutAbTiterResult] get_neut_ab_titer_result(filter_criteria_fields)

Retrieve Neutralizing Antibody Titer results using filters

Returns Neutralizing Antibody Titer results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.filter_criteria_fields import FilterCriteriaFields
from immport_client.models.v_neut_ab_titer_result import VNeutAbTiterResult
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
    api_instance = immport_client.StudyResultApi(api_client)
    filter_criteria_fields = immport_client.FilterCriteriaFields() # FilterCriteriaFields | 

    try:
        # Retrieve Neutralizing Antibody Titer results using filters
        api_response = api_instance.get_neut_ab_titer_result(filter_criteria_fields)
        print("The response of StudyResultApi->get_neut_ab_titer_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_neut_ab_titer_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_criteria_fields** | [**FilterCriteriaFields**](.md)|  | 

### Return type

[**List[VNeutAbTiterResult]**](VNeutAbTiterResult.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Neutralizaing Antibody Titer Results |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_pcr_result**
> List[VPcrResult] get_pcr_result(filter_criteria_fields)

Retrieve PCR results using filters

Returns PCR results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.filter_criteria_fields import FilterCriteriaFields
from immport_client.models.v_pcr_result import VPcrResult
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
    api_instance = immport_client.StudyResultApi(api_client)
    filter_criteria_fields = immport_client.FilterCriteriaFields() # FilterCriteriaFields | 

    try:
        # Retrieve PCR results using filters
        api_response = api_instance.get_pcr_result(filter_criteria_fields)
        print("The response of StudyResultApi->get_pcr_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_pcr_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_criteria_fields** | [**FilterCriteriaFields**](.md)|  | 

### Return type

[**List[VPcrResult]**](VPcrResult.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return PCR Results |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

