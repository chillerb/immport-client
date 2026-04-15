# immport_client.StudyDataApi

All URIs are relative to *https://immport.org/data/query*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_all_file_details_api**](StudyDataApi.md#get_all_file_details_api) | **GET** /api/study/filePath/{studyAccession} | Retrieve All File Path Information
[**get_protocol_file_details_api**](StudyDataApi.md#get_protocol_file_details_api) | **GET** /api/study/filePath/protocolFiles/{studyAccession} | Retrieve Protocol File Path Information
[**get_restricted_study_accessions**](StudyDataApi.md#get_restricted_study_accessions) | **GET** /api/study/getRestrictedStudyAccessions | 
[**get_result_file_details_api**](StudyDataApi.md#get_result_file_details_api) | **GET** /api/study/filePath/resultFiles/{studyAccession} | Retrieve Result File Path Information
[**get_study**](StudyDataApi.md#get_study) | **GET** /api/study/{studyAccession} | Retrieve Basic Study Information
[**get_study_adverse_event_api**](StudyDataApi.md#get_study_adverse_event_api) | **GET** /api/study/adverseEvent/{studyAccession} | Retrieve Study Adverse Event Information
[**get_study_arm_api**](StudyDataApi.md#get_study_arm_api) | **GET** /api/study/arm/{studyAccession} | Retrieve Study Arm Information
[**get_study_condition_or_disease**](StudyDataApi.md#get_study_condition_or_disease) | **GET** /api/study/condition/{studyAccession} | Retrieve Study ConditionOrDisease
[**get_study_contract_program**](StudyDataApi.md#get_study_contract_program) | **GET** /api/study/contract/{studyAccession} | Retrieve Study Contract and Program Information
[**get_study_experiment_api**](StudyDataApi.md#get_study_experiment_api) | **GET** /api/study/experiment/{studyAccession} | Retrieve Study Experiments
[**get_study_file_api**](StudyDataApi.md#get_study_file_api) | **GET** /api/study/file/{studyAccession} | Retrieve Study File Information
[**get_study_file_details_api**](StudyDataApi.md#get_study_file_details_api) | **GET** /api/study/filePath/studyFiles/{studyAccession} | Retrieve Study File Path Information
[**get_study_immune_exposure_api**](StudyDataApi.md#get_study_immune_exposure_api) | **GET** /api/study/immuneExposure/{studyAccession} | Retrieve Study Subject Immune Exposure Information
[**get_study_inclusion_exclusion_api**](StudyDataApi.md#get_study_inclusion_exclusion_api) | **GET** /api/study/inclusionExclusion/{studyAccession} | Retrieve Study Inclusion/Exclusion critera
[**get_study_intervention_api**](StudyDataApi.md#get_study_intervention_api) | **GET** /api/study/intervention/{studyAccession} | Retrieve Study Subject Intervention Information
[**get_study_link**](StudyDataApi.md#get_study_link) | **GET** /api/study/link/{studyAccession} | Retrieve Study Links
[**get_study_personnel**](StudyDataApi.md#get_study_personnel) | **GET** /api/study/personnel/{studyAccession} | Retrieve Study Personnel Information
[**get_study_planned_visit**](StudyDataApi.md#get_study_planned_visit) | **GET** /api/study/plannedVisit/{studyAccession} | Retrieve Planned Visit Information
[**get_study_protocol**](StudyDataApi.md#get_study_protocol) | **GET** /api/study/protocol/{studyAccession} | Retrieve Protocol Information
[**get_study_pubmed**](StudyDataApi.md#get_study_pubmed) | **GET** /api/study/pubmed/{studyAccession} | Retrieve Pubmed Information
[**get_study_subject_assessment_api**](StudyDataApi.md#get_study_subject_assessment_api) | **GET** /api/study/assessment/{studyAccession} | Retrieve Study Subject Assessments
[**get_study_subject_bio_sample_api**](StudyDataApi.md#get_study_subject_bio_sample_api) | **GET** /api/study/biosample/{studyAccession} | Retrieve Study Subject BioSample Information
[**get_study_subject_demographic_api**](StudyDataApi.md#get_study_subject_demographic_api) | **GET** /api/study/demographic/{studyAccession} | Retrieve Study Subject Demographics
[**get_study_subject_exp_sample_api**](StudyDataApi.md#get_study_subject_exp_sample_api) | **GET** /api/study/expsample/{studyAccession} | Retrieve Study Subject ExpSample Information
[**get_study_subject_lab_test_api**](StudyDataApi.md#get_study_subject_lab_test_api) | **GET** /api/study/labtest/{studyAccession} | Retrieve Study Subject Lab Tests
[**get_study_summary**](StudyDataApi.md#get_study_summary) | **GET** /api/study/summary/{studyAccession} | 


# **get_all_file_details_api**
> List[StudyFileDetailsApi] get_all_file_details_api(study_accession, format=format)

Retrieve All File Path Information

Return All File Path Information for one study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_file_details_api import StudyFileDetailsApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve All File Path Information
        api_response = api_instance.get_all_file_details_api(study_accession, format=format)
        print("The response of StudyDataApi->get_all_file_details_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_all_file_details_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyFileDetailsApi]**](StudyFileDetailsApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return All File Path Information |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_protocol_file_details_api**
> List[StudyFileDetailsApi] get_protocol_file_details_api(study_accession, format=format)

Retrieve Protocol File Path Information

Return Protocol File Path Information for one study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_file_details_api import StudyFileDetailsApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Protocol File Path Information
        api_response = api_instance.get_protocol_file_details_api(study_accession, format=format)
        print("The response of StudyDataApi->get_protocol_file_details_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_protocol_file_details_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyFileDetailsApi]**](StudyFileDetailsApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Protocol File Path Information |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_restricted_study_accessions**
> List[str] get_restricted_study_accessions()

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
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
    api_instance = immport_client.StudyDataApi(api_client)

    try:
        api_response = api_instance.get_restricted_study_accessions()
        print("The response of StudyDataApi->get_restricted_study_accessions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_restricted_study_accessions: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**List[str]**

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_result_file_details_api**
> List[StudyFileDetailsApi] get_result_file_details_api(study_accession, format=format)

Retrieve Result File Path Information

Return Result File Path Information for one study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_file_details_api import StudyFileDetailsApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Result File Path Information
        api_response = api_instance.get_result_file_details_api(study_accession, format=format)
        print("The response of StudyDataApi->get_result_file_details_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_result_file_details_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyFileDetailsApi]**](StudyFileDetailsApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Result File Path Information |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study**
> List[StudyApi] get_study(study_accession, format=format)

Retrieve Basic Study Information

Returns basic information for the Study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_api import StudyApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Basic Study Information
        api_response = api_instance.get_study(study_accession, format=format)
        print("The response of StudyDataApi->get_study:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyApi]**](StudyApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Study Information |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_adverse_event_api**
> List[StudyAdverseEventApi] get_study_adverse_event_api(study_accession, format=format)

Retrieve Study Adverse Event Information

Return Study Adverse Event information for one study. **WARNING**: This endpoint can return so much data the Web page may time out or fail.

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_adverse_event_api import StudyAdverseEventApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1231' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Adverse Event Information
        api_response = api_instance.get_study_adverse_event_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_adverse_event_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_adverse_event_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyAdverseEventApi]**](StudyAdverseEventApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Study Adverse Event Information |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_arm_api**
> List[StudyArmApi] get_study_arm_api(study_accession, format=format)

Retrieve Study Arm Information

Return Study Arm information for one study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_arm_api import StudyArmApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Arm Information
        api_response = api_instance.get_study_arm_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_arm_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_arm_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyArmApi]**](StudyArmApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Study Arm Information |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_condition_or_disease**
> List[StudyConditionOrDiseaseApi] get_study_condition_or_disease(study_accession, format=format)

Retrieve Study ConditionOrDisease

Returns the Condition or Diseases link for the Study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_condition_or_disease_api import StudyConditionOrDiseaseApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study ConditionOrDisease
        api_response = api_instance.get_study_condition_or_disease(study_accession, format=format)
        print("The response of StudyDataApi->get_study_condition_or_disease:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_condition_or_disease: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyConditionOrDiseaseApi]**](StudyConditionOrDiseaseApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Study Condition or Disease |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_contract_program**
> List[StudyContractProgramApi] get_study_contract_program(study_accession, format=format)

Retrieve Study Contract and Program Information

Returns the Contract and Program information for the Study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_contract_program_api import StudyContractProgramApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Contract and Program Information
        api_response = api_instance.get_study_contract_program(study_accession, format=format)
        print("The response of StudyDataApi->get_study_contract_program:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_contract_program: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyContractProgramApi]**](StudyContractProgramApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Study Contract and Program Information |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_experiment_api**
> List[StudyExperimentApi] get_study_experiment_api(study_accession, format=format)

Retrieve Study Experiments

Return Experiments for one study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_experiment_api import StudyExperimentApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Experiments
        api_response = api_instance.get_study_experiment_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_experiment_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_experiment_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyExperimentApi]**](StudyExperimentApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Experiments |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_file_api**
> List[StudyFileApi] get_study_file_api(study_accession, format=format)

Retrieve Study File Information

Return Study File Information for one study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_file_api import StudyFileApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study File Information
        api_response = api_instance.get_study_file_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_file_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_file_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyFileApi]**](StudyFileApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Study File Information |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_file_details_api**
> List[StudyFileDetailsApi] get_study_file_details_api(study_accession, format=format)

Retrieve Study File Path Information

Return Study File Path Information for one study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_file_details_api import StudyFileDetailsApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study File Path Information
        api_response = api_instance.get_study_file_details_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_file_details_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_file_details_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyFileDetailsApi]**](StudyFileDetailsApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Study File Path Information |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_immune_exposure_api**
> List[StudySubjectImmuneExposureApi] get_study_immune_exposure_api(study_accession, format=format)

Retrieve Study Subject Immune Exposure Information

Return Study Subject Immune Exposure Information. **WARNING**: This endpoint can return so much data the Web page may time out or fail.

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_subject_immune_exposure_api import StudySubjectImmuneExposureApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1230' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Subject Immune Exposure Information
        api_response = api_instance.get_study_immune_exposure_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_immune_exposure_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_immune_exposure_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudySubjectImmuneExposureApi]**](StudySubjectImmuneExposureApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Study Subject Immune Exposure Information |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_inclusion_exclusion_api**
> List[StudyInclusionExclusionApi] get_study_inclusion_exclusion_api(study_accession, format=format)

Retrieve Study Inclusion/Exclusion critera

Return Study Inclusion/Exclustion critera for one study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_inclusion_exclusion_api import StudyInclusionExclusionApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Inclusion/Exclusion critera
        api_response = api_instance.get_study_inclusion_exclusion_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_inclusion_exclusion_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_inclusion_exclusion_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyInclusionExclusionApi]**](StudyInclusionExclusionApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Study Inclusion/Exclusion criteria |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_intervention_api**
> List[StudySubjectInterventionApi] get_study_intervention_api(study_accession, format=format)

Retrieve Study Subject Intervention Information

Return Study Subject Intervention Information. **WARNING**: This endpoint can return so much data the Web page may time out or fail.

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_subject_intervention_api import StudySubjectInterventionApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1597' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Subject Intervention Information
        api_response = api_instance.get_study_intervention_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_intervention_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_intervention_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudySubjectInterventionApi]**](StudySubjectInterventionApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Study Subject Intervention Information |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_link**
> List[StudyLinkApi] get_study_link(study_accession, format=format)

Retrieve Study Links

Returns the external links for the Study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_link_api import StudyLinkApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Links
        api_response = api_instance.get_study_link(study_accession, format=format)
        print("The response of StudyDataApi->get_study_link:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_link: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyLinkApi]**](StudyLinkApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Links |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_personnel**
> List[StudyPersonnelApi] get_study_personnel(study_accession, format=format)

Retrieve Study Personnel Information

Returns the Personnel Information for the Study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_personnel_api import StudyPersonnelApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Personnel Information
        api_response = api_instance.get_study_personnel(study_accession, format=format)
        print("The response of StudyDataApi->get_study_personnel:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_personnel: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyPersonnelApi]**](StudyPersonnelApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Study Personnel |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_planned_visit**
> List[StudyPlannedVisitApi] get_study_planned_visit(study_accession, format=format)

Retrieve Planned Visit Information

Returns the Planned Visit Information for the Study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_planned_visit_api import StudyPlannedVisitApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Planned Visit Information
        api_response = api_instance.get_study_planned_visit(study_accession, format=format)
        print("The response of StudyDataApi->get_study_planned_visit:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_planned_visit: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyPlannedVisitApi]**](StudyPlannedVisitApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Study Planned Visits |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_protocol**
> List[StudyProtocolApi] get_study_protocol(study_accession, format=format)

Retrieve Protocol Information

Returns the Protocol Information for the Study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_protocol_api import StudyProtocolApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Protocol Information
        api_response = api_instance.get_study_protocol(study_accession, format=format)
        print("The response of StudyDataApi->get_study_protocol:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_protocol: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyProtocolApi]**](StudyProtocolApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Study Protocol Information |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_pubmed**
> List[StudyPubmedApi] get_study_pubmed(study_accession, format=format)

Retrieve Pubmed Information

Returns the Pubmed Information for the Study

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_pubmed_api import StudyPubmedApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Pubmed Information
        api_response = api_instance.get_study_pubmed(study_accession, format=format)
        print("The response of StudyDataApi->get_study_pubmed:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_pubmed: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudyPubmedApi]**](StudyPubmedApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Study Pubmed Information |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_subject_assessment_api**
> List[StudySubjectAssessmentsApi] get_study_subject_assessment_api(study_accession, format=format)

Retrieve Study Subject Assessments

Return Subject assessments for one study. Joins the Study->Arm_Or_Cohort->Arm_2_Subject-> Subject -> Assessment Tables **WARNING**: This endpoint can return so much data the Web page may time out or fail.

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_subject_assessments_api import StudySubjectAssessmentsApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1475' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Subject Assessments
        api_response = api_instance.get_study_subject_assessment_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_subject_assessment_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_subject_assessment_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudySubjectAssessmentsApi]**](StudySubjectAssessmentsApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Subject Assessments |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_subject_bio_sample_api**
> List[StudySubjectBioSampleApi] get_study_subject_bio_sample_api(study_accession, format=format)

Retrieve Study Subject BioSample Information

Return Subject/BioSample for one study. Joins the Study->Arm_Or_Cohort->Arm_2_Subject-> Subject->BioSample Tables. **WARNING**: This endpoint can return so much data the Web page may time out or fail.

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_subject_bio_sample_api import StudySubjectBioSampleApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1092' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Subject BioSample Information
        api_response = api_instance.get_study_subject_bio_sample_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_subject_bio_sample_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_subject_bio_sample_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudySubjectBioSampleApi]**](StudySubjectBioSampleApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Subject Biosample Informaiton |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_subject_demographic_api**
> List[StudySubjectDemographicsApi] get_study_subject_demographic_api(study_accession, format=format)

Retrieve Study Subject Demographics

Return Subject demographics for one study. Joins the Study->Arm_Or_Cohort->Arm_2_Subject-> Subject Tables. **WARNING**: This endpoint can return so much data the Web page may time out or fail.

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_subject_demographics_api import StudySubjectDemographicsApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1475' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Subject Demographics
        api_response = api_instance.get_study_subject_demographic_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_subject_demographic_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_subject_demographic_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudySubjectDemographicsApi]**](StudySubjectDemographicsApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Subject Demographics |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_subject_exp_sample_api**
> List[StudySubjectExpSampleApi] get_study_subject_exp_sample_api(study_accession, format=format)

Retrieve Study Subject ExpSample Information

Return Subject/ExpSample for one study. Joins the Study->Arm_Or_Cohort->Arm_2_Subject-> Subject->BioSample-Experiment->Expsample Tables. \n\n**WARNING**: This endpoint can return so much data the Web page may time out or fail.

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_subject_exp_sample_api import StudySubjectExpSampleApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY1092' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Subject ExpSample Information
        api_response = api_instance.get_study_subject_exp_sample_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_subject_exp_sample_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_subject_exp_sample_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudySubjectExpSampleApi]**](StudySubjectExpSampleApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**403** | Not Authorized, must include Token |  -  |
**200** | Return Subject ExpSample Informaiton |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_subject_lab_test_api**
> List[StudySubjectLabTestsApi] get_study_subject_lab_test_api(study_accession, format=format)

Retrieve Study Subject Lab Tests

Return Subject Lab Tests for one study. Joins the Study->Arm_Or_Cohort->Arm_2_Subject-> Subject -> Lab_Test_Panel -> Lab_Test Tables **WARNING**: This endpoint can return so much data the Web page may time out or fail.

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_subject_lab_tests_api import StudySubjectLabTestsApi
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'SDY305' # str | 
    format = 'json' # str |  (optional)

    try:
        # Retrieve Study Subject Lab Tests
        api_response = api_instance.get_study_subject_lab_test_api(study_accession, format=format)
        print("The response of StudyDataApi->get_study_subject_lab_test_api:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_subject_lab_test_api: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 
 **format** | **str**|  | [optional] 

### Return type

[**List[StudySubjectLabTestsApi]**](StudySubjectLabTestsApi.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/tab-separated-values

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return Subject Lab Tests |  -  |
**403** | Not Authorized, must include Token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_study_summary**
> StudySummary get_study_summary(study_accession)

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
from immport_client.models.study_summary import StudySummary
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
    api_instance = immport_client.StudyDataApi(api_client)
    study_accession = 'study_accession_example' # str | 

    try:
        api_response = api_instance.get_study_summary(study_accession)
        print("The response of StudyDataApi->get_study_summary:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyDataApi->get_study_summary: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **study_accession** | **str**|  | 

### Return type

[**StudySummary**](StudySummary.md)

### Authorization

[immport-security](../README.md#immport-security)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

