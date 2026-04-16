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
> List[VElisaResult] get_elisa_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)

Retrieve ELISA results using filters

Returns ELISA results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
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
    age_event = ['age_event_example'] # List[str] |  (optional)
    age_event_specify = ['age_event_specify_example'] # List[str] |  (optional)
    age_unit = ['age_unit_example'] # List[str] |  (optional)
    ancestral_population = ['ancestral_population_example'] # List[str] |  (optional)
    arm_accession = ['arm_accession_example'] # List[str] |  (optional)
    arm_name = ['arm_name_example'] # List[str] |  (optional)
    biosample_accession = ['biosample_accession_example'] # List[str] |  (optional)
    biosample_subtype = ['biosample_subtype_example'] # List[str] |  (optional)
    biosample_type = ['biosample_type_example'] # List[str] |  (optional)
    clinical = 'clinical_example' # str |  (optional)
    ethnicity = ['ethnicity_example'] # List[str] |  (optional)
    experiment_accession = ['experiment_accession_example'] # List[str] |  (optional)
    expsample_accession = ['expsample_accession_example'] # List[str] |  (optional)
    gender = ['gender_example'] # List[str] |  (optional)
    sex = ['sex_example'] # List[str] |  (optional)
    max_subject_age = 3.4 # float |  (optional)
    max_subject_age_gte = 3.4 # float |  (optional)
    max_subject_age_lte = 3.4 # float |  (optional)
    max_subject_age_gt = 3.4 # float |  (optional)
    max_subject_age_lt = 3.4 # float |  (optional)
    min_subject_age = 3.4 # float |  (optional)
    min_subject_age_gte = 3.4 # float |  (optional)
    min_subject_age_lte = 3.4 # float |  (optional)
    min_subject_age_gt = 3.4 # float |  (optional)
    min_subject_age_lt = 3.4 # float |  (optional)
    measurement_technique = ['measurement_technique_example'] # List[str] |  (optional)
    planned_visit_accession = ['planned_visit_accession_example'] # List[str] |  (optional)
    race = ['race_example'] # List[str] |  (optional)
    race_specify = ['race_specify_example'] # List[str] |  (optional)
    species = ['species_example'] # List[str] |  (optional)
    strain = ['strain_example'] # List[str] |  (optional)
    study_accession = ['study_accession_example'] # List[str] |  (optional)
    study_time_collected = 3.4 # float |  (optional)
    study_time_collected_gte = 3.4 # float |  (optional)
    study_time_collected_lte = 3.4 # float |  (optional)
    study_time_collected_gt = 3.4 # float |  (optional)
    study_time_collected_lt = 3.4 # float |  (optional)
    study_time_collected_unit = ['study_time_collected_unit_example'] # List[str] |  (optional)
    study_time_t0_event = ['study_time_t0_event_example'] # List[str] |  (optional)
    study_time_t0_event_specify = ['study_time_t0_event_specify_example'] # List[str] |  (optional)
    subject_accession = ['subject_accession_example'] # List[str] |  (optional)
    study_title = ['study_title_example'] # List[str] |  (optional)
    subject_phenotype = ['subject_phenotype_example'] # List[str] |  (optional)
    treatment_accession = ['treatment_accession_example'] # List[str] |  (optional)
    format = 'format_example' # str |  (optional)

    try:
        # Retrieve ELISA results using filters
        api_response = api_instance.get_elisa_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)
        print("The response of StudyResultApi->get_elisa_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_elisa_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **age_event** | [**List[str]**](str.md)|  | [optional] 
 **age_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **age_unit** | [**List[str]**](str.md)|  | [optional] 
 **ancestral_population** | [**List[str]**](str.md)|  | [optional] 
 **arm_accession** | [**List[str]**](str.md)|  | [optional] 
 **arm_name** | [**List[str]**](str.md)|  | [optional] 
 **biosample_accession** | [**List[str]**](str.md)|  | [optional] 
 **biosample_subtype** | [**List[str]**](str.md)|  | [optional] 
 **biosample_type** | [**List[str]**](str.md)|  | [optional] 
 **clinical** | **str**|  | [optional] 
 **ethnicity** | [**List[str]**](str.md)|  | [optional] 
 **experiment_accession** | [**List[str]**](str.md)|  | [optional] 
 **expsample_accession** | [**List[str]**](str.md)|  | [optional] 
 **gender** | [**List[str]**](str.md)|  | [optional] 
 **sex** | [**List[str]**](str.md)|  | [optional] 
 **max_subject_age** | **float**|  | [optional] 
 **max_subject_age_gte** | **float**|  | [optional] 
 **max_subject_age_lte** | **float**|  | [optional] 
 **max_subject_age_gt** | **float**|  | [optional] 
 **max_subject_age_lt** | **float**|  | [optional] 
 **min_subject_age** | **float**|  | [optional] 
 **min_subject_age_gte** | **float**|  | [optional] 
 **min_subject_age_lte** | **float**|  | [optional] 
 **min_subject_age_gt** | **float**|  | [optional] 
 **min_subject_age_lt** | **float**|  | [optional] 
 **measurement_technique** | [**List[str]**](str.md)|  | [optional] 
 **planned_visit_accession** | [**List[str]**](str.md)|  | [optional] 
 **race** | [**List[str]**](str.md)|  | [optional] 
 **race_specify** | [**List[str]**](str.md)|  | [optional] 
 **species** | [**List[str]**](str.md)|  | [optional] 
 **strain** | [**List[str]**](str.md)|  | [optional] 
 **study_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_time_collected** | **float**|  | [optional] 
 **study_time_collected_gte** | **float**|  | [optional] 
 **study_time_collected_lte** | **float**|  | [optional] 
 **study_time_collected_gt** | **float**|  | [optional] 
 **study_time_collected_lt** | **float**|  | [optional] 
 **study_time_collected_unit** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **subject_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_title** | [**List[str]**](str.md)|  | [optional] 
 **subject_phenotype** | [**List[str]**](str.md)|  | [optional] 
 **treatment_accession** | [**List[str]**](str.md)|  | [optional] 
 **format** | **str**|  | [optional] 

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
> List[VElispotResult] get_elispot_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)

Retrieve Elispot results using filters

Returns Elispot results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
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
    age_event = ['age_event_example'] # List[str] |  (optional)
    age_event_specify = ['age_event_specify_example'] # List[str] |  (optional)
    age_unit = ['age_unit_example'] # List[str] |  (optional)
    ancestral_population = ['ancestral_population_example'] # List[str] |  (optional)
    arm_accession = ['arm_accession_example'] # List[str] |  (optional)
    arm_name = ['arm_name_example'] # List[str] |  (optional)
    biosample_accession = ['biosample_accession_example'] # List[str] |  (optional)
    biosample_subtype = ['biosample_subtype_example'] # List[str] |  (optional)
    biosample_type = ['biosample_type_example'] # List[str] |  (optional)
    clinical = 'clinical_example' # str |  (optional)
    ethnicity = ['ethnicity_example'] # List[str] |  (optional)
    experiment_accession = ['experiment_accession_example'] # List[str] |  (optional)
    expsample_accession = ['expsample_accession_example'] # List[str] |  (optional)
    gender = ['gender_example'] # List[str] |  (optional)
    sex = ['sex_example'] # List[str] |  (optional)
    max_subject_age = 3.4 # float |  (optional)
    max_subject_age_gte = 3.4 # float |  (optional)
    max_subject_age_lte = 3.4 # float |  (optional)
    max_subject_age_gt = 3.4 # float |  (optional)
    max_subject_age_lt = 3.4 # float |  (optional)
    min_subject_age = 3.4 # float |  (optional)
    min_subject_age_gte = 3.4 # float |  (optional)
    min_subject_age_lte = 3.4 # float |  (optional)
    min_subject_age_gt = 3.4 # float |  (optional)
    min_subject_age_lt = 3.4 # float |  (optional)
    measurement_technique = ['measurement_technique_example'] # List[str] |  (optional)
    planned_visit_accession = ['planned_visit_accession_example'] # List[str] |  (optional)
    race = ['race_example'] # List[str] |  (optional)
    race_specify = ['race_specify_example'] # List[str] |  (optional)
    species = ['species_example'] # List[str] |  (optional)
    strain = ['strain_example'] # List[str] |  (optional)
    study_accession = ['study_accession_example'] # List[str] |  (optional)
    study_time_collected = 3.4 # float |  (optional)
    study_time_collected_gte = 3.4 # float |  (optional)
    study_time_collected_lte = 3.4 # float |  (optional)
    study_time_collected_gt = 3.4 # float |  (optional)
    study_time_collected_lt = 3.4 # float |  (optional)
    study_time_collected_unit = ['study_time_collected_unit_example'] # List[str] |  (optional)
    study_time_t0_event = ['study_time_t0_event_example'] # List[str] |  (optional)
    study_time_t0_event_specify = ['study_time_t0_event_specify_example'] # List[str] |  (optional)
    subject_accession = ['subject_accession_example'] # List[str] |  (optional)
    study_title = ['study_title_example'] # List[str] |  (optional)
    subject_phenotype = ['subject_phenotype_example'] # List[str] |  (optional)
    treatment_accession = ['treatment_accession_example'] # List[str] |  (optional)
    format = 'format_example' # str |  (optional)

    try:
        # Retrieve Elispot results using filters
        api_response = api_instance.get_elispot_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)
        print("The response of StudyResultApi->get_elispot_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_elispot_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **age_event** | [**List[str]**](str.md)|  | [optional] 
 **age_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **age_unit** | [**List[str]**](str.md)|  | [optional] 
 **ancestral_population** | [**List[str]**](str.md)|  | [optional] 
 **arm_accession** | [**List[str]**](str.md)|  | [optional] 
 **arm_name** | [**List[str]**](str.md)|  | [optional] 
 **biosample_accession** | [**List[str]**](str.md)|  | [optional] 
 **biosample_subtype** | [**List[str]**](str.md)|  | [optional] 
 **biosample_type** | [**List[str]**](str.md)|  | [optional] 
 **clinical** | **str**|  | [optional] 
 **ethnicity** | [**List[str]**](str.md)|  | [optional] 
 **experiment_accession** | [**List[str]**](str.md)|  | [optional] 
 **expsample_accession** | [**List[str]**](str.md)|  | [optional] 
 **gender** | [**List[str]**](str.md)|  | [optional] 
 **sex** | [**List[str]**](str.md)|  | [optional] 
 **max_subject_age** | **float**|  | [optional] 
 **max_subject_age_gte** | **float**|  | [optional] 
 **max_subject_age_lte** | **float**|  | [optional] 
 **max_subject_age_gt** | **float**|  | [optional] 
 **max_subject_age_lt** | **float**|  | [optional] 
 **min_subject_age** | **float**|  | [optional] 
 **min_subject_age_gte** | **float**|  | [optional] 
 **min_subject_age_lte** | **float**|  | [optional] 
 **min_subject_age_gt** | **float**|  | [optional] 
 **min_subject_age_lt** | **float**|  | [optional] 
 **measurement_technique** | [**List[str]**](str.md)|  | [optional] 
 **planned_visit_accession** | [**List[str]**](str.md)|  | [optional] 
 **race** | [**List[str]**](str.md)|  | [optional] 
 **race_specify** | [**List[str]**](str.md)|  | [optional] 
 **species** | [**List[str]**](str.md)|  | [optional] 
 **strain** | [**List[str]**](str.md)|  | [optional] 
 **study_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_time_collected** | **float**|  | [optional] 
 **study_time_collected_gte** | **float**|  | [optional] 
 **study_time_collected_lte** | **float**|  | [optional] 
 **study_time_collected_gt** | **float**|  | [optional] 
 **study_time_collected_lt** | **float**|  | [optional] 
 **study_time_collected_unit** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **subject_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_title** | [**List[str]**](str.md)|  | [optional] 
 **subject_phenotype** | [**List[str]**](str.md)|  | [optional] 
 **treatment_accession** | [**List[str]**](str.md)|  | [optional] 
 **format** | **str**|  | [optional] 

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
> List[VFcsAnalyzedResult] get_fcs_analyzed_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)

Retrieve FcsAnalyzed results using filters

Returns FcsAnalyzed results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
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
    age_event = ['age_event_example'] # List[str] |  (optional)
    age_event_specify = ['age_event_specify_example'] # List[str] |  (optional)
    age_unit = ['age_unit_example'] # List[str] |  (optional)
    ancestral_population = ['ancestral_population_example'] # List[str] |  (optional)
    arm_accession = ['arm_accession_example'] # List[str] |  (optional)
    arm_name = ['arm_name_example'] # List[str] |  (optional)
    biosample_accession = ['biosample_accession_example'] # List[str] |  (optional)
    biosample_subtype = ['biosample_subtype_example'] # List[str] |  (optional)
    biosample_type = ['biosample_type_example'] # List[str] |  (optional)
    clinical = 'clinical_example' # str |  (optional)
    ethnicity = ['ethnicity_example'] # List[str] |  (optional)
    experiment_accession = ['experiment_accession_example'] # List[str] |  (optional)
    expsample_accession = ['expsample_accession_example'] # List[str] |  (optional)
    gender = ['gender_example'] # List[str] |  (optional)
    sex = ['sex_example'] # List[str] |  (optional)
    max_subject_age = 3.4 # float |  (optional)
    max_subject_age_gte = 3.4 # float |  (optional)
    max_subject_age_lte = 3.4 # float |  (optional)
    max_subject_age_gt = 3.4 # float |  (optional)
    max_subject_age_lt = 3.4 # float |  (optional)
    min_subject_age = 3.4 # float |  (optional)
    min_subject_age_gte = 3.4 # float |  (optional)
    min_subject_age_lte = 3.4 # float |  (optional)
    min_subject_age_gt = 3.4 # float |  (optional)
    min_subject_age_lt = 3.4 # float |  (optional)
    measurement_technique = ['measurement_technique_example'] # List[str] |  (optional)
    planned_visit_accession = ['planned_visit_accession_example'] # List[str] |  (optional)
    race = ['race_example'] # List[str] |  (optional)
    race_specify = ['race_specify_example'] # List[str] |  (optional)
    species = ['species_example'] # List[str] |  (optional)
    strain = ['strain_example'] # List[str] |  (optional)
    study_accession = ['study_accession_example'] # List[str] |  (optional)
    study_time_collected = 3.4 # float |  (optional)
    study_time_collected_gte = 3.4 # float |  (optional)
    study_time_collected_lte = 3.4 # float |  (optional)
    study_time_collected_gt = 3.4 # float |  (optional)
    study_time_collected_lt = 3.4 # float |  (optional)
    study_time_collected_unit = ['study_time_collected_unit_example'] # List[str] |  (optional)
    study_time_t0_event = ['study_time_t0_event_example'] # List[str] |  (optional)
    study_time_t0_event_specify = ['study_time_t0_event_specify_example'] # List[str] |  (optional)
    subject_accession = ['subject_accession_example'] # List[str] |  (optional)
    study_title = ['study_title_example'] # List[str] |  (optional)
    subject_phenotype = ['subject_phenotype_example'] # List[str] |  (optional)
    treatment_accession = ['treatment_accession_example'] # List[str] |  (optional)
    format = 'format_example' # str |  (optional)

    try:
        # Retrieve FcsAnalyzed results using filters
        api_response = api_instance.get_fcs_analyzed_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)
        print("The response of StudyResultApi->get_fcs_analyzed_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_fcs_analyzed_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **age_event** | [**List[str]**](str.md)|  | [optional] 
 **age_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **age_unit** | [**List[str]**](str.md)|  | [optional] 
 **ancestral_population** | [**List[str]**](str.md)|  | [optional] 
 **arm_accession** | [**List[str]**](str.md)|  | [optional] 
 **arm_name** | [**List[str]**](str.md)|  | [optional] 
 **biosample_accession** | [**List[str]**](str.md)|  | [optional] 
 **biosample_subtype** | [**List[str]**](str.md)|  | [optional] 
 **biosample_type** | [**List[str]**](str.md)|  | [optional] 
 **clinical** | **str**|  | [optional] 
 **ethnicity** | [**List[str]**](str.md)|  | [optional] 
 **experiment_accession** | [**List[str]**](str.md)|  | [optional] 
 **expsample_accession** | [**List[str]**](str.md)|  | [optional] 
 **gender** | [**List[str]**](str.md)|  | [optional] 
 **sex** | [**List[str]**](str.md)|  | [optional] 
 **max_subject_age** | **float**|  | [optional] 
 **max_subject_age_gte** | **float**|  | [optional] 
 **max_subject_age_lte** | **float**|  | [optional] 
 **max_subject_age_gt** | **float**|  | [optional] 
 **max_subject_age_lt** | **float**|  | [optional] 
 **min_subject_age** | **float**|  | [optional] 
 **min_subject_age_gte** | **float**|  | [optional] 
 **min_subject_age_lte** | **float**|  | [optional] 
 **min_subject_age_gt** | **float**|  | [optional] 
 **min_subject_age_lt** | **float**|  | [optional] 
 **measurement_technique** | [**List[str]**](str.md)|  | [optional] 
 **planned_visit_accession** | [**List[str]**](str.md)|  | [optional] 
 **race** | [**List[str]**](str.md)|  | [optional] 
 **race_specify** | [**List[str]**](str.md)|  | [optional] 
 **species** | [**List[str]**](str.md)|  | [optional] 
 **strain** | [**List[str]**](str.md)|  | [optional] 
 **study_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_time_collected** | **float**|  | [optional] 
 **study_time_collected_gte** | **float**|  | [optional] 
 **study_time_collected_lte** | **float**|  | [optional] 
 **study_time_collected_gt** | **float**|  | [optional] 
 **study_time_collected_lt** | **float**|  | [optional] 
 **study_time_collected_unit** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **subject_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_title** | [**List[str]**](str.md)|  | [optional] 
 **subject_phenotype** | [**List[str]**](str.md)|  | [optional] 
 **treatment_accession** | [**List[str]**](str.md)|  | [optional] 
 **format** | **str**|  | [optional] 

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
> List[VResultFilePath] get_file_path(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)

Retrieve File Paths using filters

Returns File Paths based on filter criteria
These paths represent file locations within the ImmPort SharedData File system.
Review the File Download tutorial to see how to use these Paths to retrieve the file.

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
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
    age_event = ['age_event_example'] # List[str] |  (optional)
    age_event_specify = ['age_event_specify_example'] # List[str] |  (optional)
    age_unit = ['age_unit_example'] # List[str] |  (optional)
    ancestral_population = ['ancestral_population_example'] # List[str] |  (optional)
    arm_accession = ['arm_accession_example'] # List[str] |  (optional)
    arm_name = ['arm_name_example'] # List[str] |  (optional)
    biosample_accession = ['biosample_accession_example'] # List[str] |  (optional)
    biosample_subtype = ['biosample_subtype_example'] # List[str] |  (optional)
    biosample_type = ['biosample_type_example'] # List[str] |  (optional)
    clinical = 'clinical_example' # str |  (optional)
    ethnicity = ['ethnicity_example'] # List[str] |  (optional)
    experiment_accession = ['experiment_accession_example'] # List[str] |  (optional)
    expsample_accession = ['expsample_accession_example'] # List[str] |  (optional)
    gender = ['gender_example'] # List[str] |  (optional)
    sex = ['sex_example'] # List[str] |  (optional)
    max_subject_age = 3.4 # float |  (optional)
    max_subject_age_gte = 3.4 # float |  (optional)
    max_subject_age_lte = 3.4 # float |  (optional)
    max_subject_age_gt = 3.4 # float |  (optional)
    max_subject_age_lt = 3.4 # float |  (optional)
    min_subject_age = 3.4 # float |  (optional)
    min_subject_age_gte = 3.4 # float |  (optional)
    min_subject_age_lte = 3.4 # float |  (optional)
    min_subject_age_gt = 3.4 # float |  (optional)
    min_subject_age_lt = 3.4 # float |  (optional)
    measurement_technique = ['measurement_technique_example'] # List[str] |  (optional)
    planned_visit_accession = ['planned_visit_accession_example'] # List[str] |  (optional)
    race = ['race_example'] # List[str] |  (optional)
    race_specify = ['race_specify_example'] # List[str] |  (optional)
    species = ['species_example'] # List[str] |  (optional)
    strain = ['strain_example'] # List[str] |  (optional)
    study_accession = ['study_accession_example'] # List[str] |  (optional)
    study_time_collected = 3.4 # float |  (optional)
    study_time_collected_gte = 3.4 # float |  (optional)
    study_time_collected_lte = 3.4 # float |  (optional)
    study_time_collected_gt = 3.4 # float |  (optional)
    study_time_collected_lt = 3.4 # float |  (optional)
    study_time_collected_unit = ['study_time_collected_unit_example'] # List[str] |  (optional)
    study_time_t0_event = ['study_time_t0_event_example'] # List[str] |  (optional)
    study_time_t0_event_specify = ['study_time_t0_event_specify_example'] # List[str] |  (optional)
    subject_accession = ['subject_accession_example'] # List[str] |  (optional)
    study_title = ['study_title_example'] # List[str] |  (optional)
    subject_phenotype = ['subject_phenotype_example'] # List[str] |  (optional)
    treatment_accession = ['treatment_accession_example'] # List[str] |  (optional)
    format = 'format_example' # str |  (optional)

    try:
        # Retrieve File Paths using filters
        api_response = api_instance.get_file_path(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)
        print("The response of StudyResultApi->get_file_path:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_file_path: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **age_event** | [**List[str]**](str.md)|  | [optional] 
 **age_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **age_unit** | [**List[str]**](str.md)|  | [optional] 
 **ancestral_population** | [**List[str]**](str.md)|  | [optional] 
 **arm_accession** | [**List[str]**](str.md)|  | [optional] 
 **arm_name** | [**List[str]**](str.md)|  | [optional] 
 **biosample_accession** | [**List[str]**](str.md)|  | [optional] 
 **biosample_subtype** | [**List[str]**](str.md)|  | [optional] 
 **biosample_type** | [**List[str]**](str.md)|  | [optional] 
 **clinical** | **str**|  | [optional] 
 **ethnicity** | [**List[str]**](str.md)|  | [optional] 
 **experiment_accession** | [**List[str]**](str.md)|  | [optional] 
 **expsample_accession** | [**List[str]**](str.md)|  | [optional] 
 **gender** | [**List[str]**](str.md)|  | [optional] 
 **sex** | [**List[str]**](str.md)|  | [optional] 
 **max_subject_age** | **float**|  | [optional] 
 **max_subject_age_gte** | **float**|  | [optional] 
 **max_subject_age_lte** | **float**|  | [optional] 
 **max_subject_age_gt** | **float**|  | [optional] 
 **max_subject_age_lt** | **float**|  | [optional] 
 **min_subject_age** | **float**|  | [optional] 
 **min_subject_age_gte** | **float**|  | [optional] 
 **min_subject_age_lte** | **float**|  | [optional] 
 **min_subject_age_gt** | **float**|  | [optional] 
 **min_subject_age_lt** | **float**|  | [optional] 
 **measurement_technique** | [**List[str]**](str.md)|  | [optional] 
 **planned_visit_accession** | [**List[str]**](str.md)|  | [optional] 
 **race** | [**List[str]**](str.md)|  | [optional] 
 **race_specify** | [**List[str]**](str.md)|  | [optional] 
 **species** | [**List[str]**](str.md)|  | [optional] 
 **strain** | [**List[str]**](str.md)|  | [optional] 
 **study_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_time_collected** | **float**|  | [optional] 
 **study_time_collected_gte** | **float**|  | [optional] 
 **study_time_collected_lte** | **float**|  | [optional] 
 **study_time_collected_gt** | **float**|  | [optional] 
 **study_time_collected_lt** | **float**|  | [optional] 
 **study_time_collected_unit** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **subject_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_title** | [**List[str]**](str.md)|  | [optional] 
 **subject_phenotype** | [**List[str]**](str.md)|  | [optional] 
 **treatment_accession** | [**List[str]**](str.md)|  | [optional] 
 **format** | **str**|  | [optional] 

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
> List[VHaiResult] get_hai_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)

Retrieve HAI results using filters

Returns HAI results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
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
    age_event = ['age_event_example'] # List[str] |  (optional)
    age_event_specify = ['age_event_specify_example'] # List[str] |  (optional)
    age_unit = ['age_unit_example'] # List[str] |  (optional)
    ancestral_population = ['ancestral_population_example'] # List[str] |  (optional)
    arm_accession = ['arm_accession_example'] # List[str] |  (optional)
    arm_name = ['arm_name_example'] # List[str] |  (optional)
    biosample_accession = ['biosample_accession_example'] # List[str] |  (optional)
    biosample_subtype = ['biosample_subtype_example'] # List[str] |  (optional)
    biosample_type = ['biosample_type_example'] # List[str] |  (optional)
    clinical = 'clinical_example' # str |  (optional)
    ethnicity = ['ethnicity_example'] # List[str] |  (optional)
    experiment_accession = ['experiment_accession_example'] # List[str] |  (optional)
    expsample_accession = ['expsample_accession_example'] # List[str] |  (optional)
    gender = ['gender_example'] # List[str] |  (optional)
    sex = ['sex_example'] # List[str] |  (optional)
    max_subject_age = 3.4 # float |  (optional)
    max_subject_age_gte = 3.4 # float |  (optional)
    max_subject_age_lte = 3.4 # float |  (optional)
    max_subject_age_gt = 3.4 # float |  (optional)
    max_subject_age_lt = 3.4 # float |  (optional)
    min_subject_age = 3.4 # float |  (optional)
    min_subject_age_gte = 3.4 # float |  (optional)
    min_subject_age_lte = 3.4 # float |  (optional)
    min_subject_age_gt = 3.4 # float |  (optional)
    min_subject_age_lt = 3.4 # float |  (optional)
    measurement_technique = ['measurement_technique_example'] # List[str] |  (optional)
    planned_visit_accession = ['planned_visit_accession_example'] # List[str] |  (optional)
    race = ['race_example'] # List[str] |  (optional)
    race_specify = ['race_specify_example'] # List[str] |  (optional)
    species = ['species_example'] # List[str] |  (optional)
    strain = ['strain_example'] # List[str] |  (optional)
    study_accession = ['study_accession_example'] # List[str] |  (optional)
    study_time_collected = 3.4 # float |  (optional)
    study_time_collected_gte = 3.4 # float |  (optional)
    study_time_collected_lte = 3.4 # float |  (optional)
    study_time_collected_gt = 3.4 # float |  (optional)
    study_time_collected_lt = 3.4 # float |  (optional)
    study_time_collected_unit = ['study_time_collected_unit_example'] # List[str] |  (optional)
    study_time_t0_event = ['study_time_t0_event_example'] # List[str] |  (optional)
    study_time_t0_event_specify = ['study_time_t0_event_specify_example'] # List[str] |  (optional)
    subject_accession = ['subject_accession_example'] # List[str] |  (optional)
    study_title = ['study_title_example'] # List[str] |  (optional)
    subject_phenotype = ['subject_phenotype_example'] # List[str] |  (optional)
    treatment_accession = ['treatment_accession_example'] # List[str] |  (optional)
    format = 'format_example' # str |  (optional)

    try:
        # Retrieve HAI results using filters
        api_response = api_instance.get_hai_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)
        print("The response of StudyResultApi->get_hai_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_hai_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **age_event** | [**List[str]**](str.md)|  | [optional] 
 **age_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **age_unit** | [**List[str]**](str.md)|  | [optional] 
 **ancestral_population** | [**List[str]**](str.md)|  | [optional] 
 **arm_accession** | [**List[str]**](str.md)|  | [optional] 
 **arm_name** | [**List[str]**](str.md)|  | [optional] 
 **biosample_accession** | [**List[str]**](str.md)|  | [optional] 
 **biosample_subtype** | [**List[str]**](str.md)|  | [optional] 
 **biosample_type** | [**List[str]**](str.md)|  | [optional] 
 **clinical** | **str**|  | [optional] 
 **ethnicity** | [**List[str]**](str.md)|  | [optional] 
 **experiment_accession** | [**List[str]**](str.md)|  | [optional] 
 **expsample_accession** | [**List[str]**](str.md)|  | [optional] 
 **gender** | [**List[str]**](str.md)|  | [optional] 
 **sex** | [**List[str]**](str.md)|  | [optional] 
 **max_subject_age** | **float**|  | [optional] 
 **max_subject_age_gte** | **float**|  | [optional] 
 **max_subject_age_lte** | **float**|  | [optional] 
 **max_subject_age_gt** | **float**|  | [optional] 
 **max_subject_age_lt** | **float**|  | [optional] 
 **min_subject_age** | **float**|  | [optional] 
 **min_subject_age_gte** | **float**|  | [optional] 
 **min_subject_age_lte** | **float**|  | [optional] 
 **min_subject_age_gt** | **float**|  | [optional] 
 **min_subject_age_lt** | **float**|  | [optional] 
 **measurement_technique** | [**List[str]**](str.md)|  | [optional] 
 **planned_visit_accession** | [**List[str]**](str.md)|  | [optional] 
 **race** | [**List[str]**](str.md)|  | [optional] 
 **race_specify** | [**List[str]**](str.md)|  | [optional] 
 **species** | [**List[str]**](str.md)|  | [optional] 
 **strain** | [**List[str]**](str.md)|  | [optional] 
 **study_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_time_collected** | **float**|  | [optional] 
 **study_time_collected_gte** | **float**|  | [optional] 
 **study_time_collected_lte** | **float**|  | [optional] 
 **study_time_collected_gt** | **float**|  | [optional] 
 **study_time_collected_lt** | **float**|  | [optional] 
 **study_time_collected_unit** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **subject_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_title** | [**List[str]**](str.md)|  | [optional] 
 **subject_phenotype** | [**List[str]**](str.md)|  | [optional] 
 **treatment_accession** | [**List[str]**](str.md)|  | [optional] 
 **format** | **str**|  | [optional] 

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
> List[VHlaTypingResult] get_hla_typing_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)

Retrieve HLA Typing results using filters

Returns HLA Typing results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
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
    age_event = ['age_event_example'] # List[str] |  (optional)
    age_event_specify = ['age_event_specify_example'] # List[str] |  (optional)
    age_unit = ['age_unit_example'] # List[str] |  (optional)
    ancestral_population = ['ancestral_population_example'] # List[str] |  (optional)
    arm_accession = ['arm_accession_example'] # List[str] |  (optional)
    arm_name = ['arm_name_example'] # List[str] |  (optional)
    biosample_accession = ['biosample_accession_example'] # List[str] |  (optional)
    biosample_subtype = ['biosample_subtype_example'] # List[str] |  (optional)
    biosample_type = ['biosample_type_example'] # List[str] |  (optional)
    clinical = 'clinical_example' # str |  (optional)
    ethnicity = ['ethnicity_example'] # List[str] |  (optional)
    experiment_accession = ['experiment_accession_example'] # List[str] |  (optional)
    expsample_accession = ['expsample_accession_example'] # List[str] |  (optional)
    gender = ['gender_example'] # List[str] |  (optional)
    sex = ['sex_example'] # List[str] |  (optional)
    max_subject_age = 3.4 # float |  (optional)
    max_subject_age_gte = 3.4 # float |  (optional)
    max_subject_age_lte = 3.4 # float |  (optional)
    max_subject_age_gt = 3.4 # float |  (optional)
    max_subject_age_lt = 3.4 # float |  (optional)
    min_subject_age = 3.4 # float |  (optional)
    min_subject_age_gte = 3.4 # float |  (optional)
    min_subject_age_lte = 3.4 # float |  (optional)
    min_subject_age_gt = 3.4 # float |  (optional)
    min_subject_age_lt = 3.4 # float |  (optional)
    measurement_technique = ['measurement_technique_example'] # List[str] |  (optional)
    planned_visit_accession = ['planned_visit_accession_example'] # List[str] |  (optional)
    race = ['race_example'] # List[str] |  (optional)
    race_specify = ['race_specify_example'] # List[str] |  (optional)
    species = ['species_example'] # List[str] |  (optional)
    strain = ['strain_example'] # List[str] |  (optional)
    study_accession = ['study_accession_example'] # List[str] |  (optional)
    study_time_collected = 3.4 # float |  (optional)
    study_time_collected_gte = 3.4 # float |  (optional)
    study_time_collected_lte = 3.4 # float |  (optional)
    study_time_collected_gt = 3.4 # float |  (optional)
    study_time_collected_lt = 3.4 # float |  (optional)
    study_time_collected_unit = ['study_time_collected_unit_example'] # List[str] |  (optional)
    study_time_t0_event = ['study_time_t0_event_example'] # List[str] |  (optional)
    study_time_t0_event_specify = ['study_time_t0_event_specify_example'] # List[str] |  (optional)
    subject_accession = ['subject_accession_example'] # List[str] |  (optional)
    study_title = ['study_title_example'] # List[str] |  (optional)
    subject_phenotype = ['subject_phenotype_example'] # List[str] |  (optional)
    treatment_accession = ['treatment_accession_example'] # List[str] |  (optional)
    format = 'format_example' # str |  (optional)

    try:
        # Retrieve HLA Typing results using filters
        api_response = api_instance.get_hla_typing_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)
        print("The response of StudyResultApi->get_hla_typing_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_hla_typing_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **age_event** | [**List[str]**](str.md)|  | [optional] 
 **age_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **age_unit** | [**List[str]**](str.md)|  | [optional] 
 **ancestral_population** | [**List[str]**](str.md)|  | [optional] 
 **arm_accession** | [**List[str]**](str.md)|  | [optional] 
 **arm_name** | [**List[str]**](str.md)|  | [optional] 
 **biosample_accession** | [**List[str]**](str.md)|  | [optional] 
 **biosample_subtype** | [**List[str]**](str.md)|  | [optional] 
 **biosample_type** | [**List[str]**](str.md)|  | [optional] 
 **clinical** | **str**|  | [optional] 
 **ethnicity** | [**List[str]**](str.md)|  | [optional] 
 **experiment_accession** | [**List[str]**](str.md)|  | [optional] 
 **expsample_accession** | [**List[str]**](str.md)|  | [optional] 
 **gender** | [**List[str]**](str.md)|  | [optional] 
 **sex** | [**List[str]**](str.md)|  | [optional] 
 **max_subject_age** | **float**|  | [optional] 
 **max_subject_age_gte** | **float**|  | [optional] 
 **max_subject_age_lte** | **float**|  | [optional] 
 **max_subject_age_gt** | **float**|  | [optional] 
 **max_subject_age_lt** | **float**|  | [optional] 
 **min_subject_age** | **float**|  | [optional] 
 **min_subject_age_gte** | **float**|  | [optional] 
 **min_subject_age_lte** | **float**|  | [optional] 
 **min_subject_age_gt** | **float**|  | [optional] 
 **min_subject_age_lt** | **float**|  | [optional] 
 **measurement_technique** | [**List[str]**](str.md)|  | [optional] 
 **planned_visit_accession** | [**List[str]**](str.md)|  | [optional] 
 **race** | [**List[str]**](str.md)|  | [optional] 
 **race_specify** | [**List[str]**](str.md)|  | [optional] 
 **species** | [**List[str]**](str.md)|  | [optional] 
 **strain** | [**List[str]**](str.md)|  | [optional] 
 **study_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_time_collected** | **float**|  | [optional] 
 **study_time_collected_gte** | **float**|  | [optional] 
 **study_time_collected_lte** | **float**|  | [optional] 
 **study_time_collected_gt** | **float**|  | [optional] 
 **study_time_collected_lt** | **float**|  | [optional] 
 **study_time_collected_unit** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **subject_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_title** | [**List[str]**](str.md)|  | [optional] 
 **subject_phenotype** | [**List[str]**](str.md)|  | [optional] 
 **treatment_accession** | [**List[str]**](str.md)|  | [optional] 
 **format** | **str**|  | [optional] 

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
> List[VKirTypingResult] get_kir_typing_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)

Retrieve kIR Typing results using filters

Returns KIR Typing results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
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
    age_event = ['age_event_example'] # List[str] |  (optional)
    age_event_specify = ['age_event_specify_example'] # List[str] |  (optional)
    age_unit = ['age_unit_example'] # List[str] |  (optional)
    ancestral_population = ['ancestral_population_example'] # List[str] |  (optional)
    arm_accession = ['arm_accession_example'] # List[str] |  (optional)
    arm_name = ['arm_name_example'] # List[str] |  (optional)
    biosample_accession = ['biosample_accession_example'] # List[str] |  (optional)
    biosample_subtype = ['biosample_subtype_example'] # List[str] |  (optional)
    biosample_type = ['biosample_type_example'] # List[str] |  (optional)
    clinical = 'clinical_example' # str |  (optional)
    ethnicity = ['ethnicity_example'] # List[str] |  (optional)
    experiment_accession = ['experiment_accession_example'] # List[str] |  (optional)
    expsample_accession = ['expsample_accession_example'] # List[str] |  (optional)
    gender = ['gender_example'] # List[str] |  (optional)
    sex = ['sex_example'] # List[str] |  (optional)
    max_subject_age = 3.4 # float |  (optional)
    max_subject_age_gte = 3.4 # float |  (optional)
    max_subject_age_lte = 3.4 # float |  (optional)
    max_subject_age_gt = 3.4 # float |  (optional)
    max_subject_age_lt = 3.4 # float |  (optional)
    min_subject_age = 3.4 # float |  (optional)
    min_subject_age_gte = 3.4 # float |  (optional)
    min_subject_age_lte = 3.4 # float |  (optional)
    min_subject_age_gt = 3.4 # float |  (optional)
    min_subject_age_lt = 3.4 # float |  (optional)
    measurement_technique = ['measurement_technique_example'] # List[str] |  (optional)
    planned_visit_accession = ['planned_visit_accession_example'] # List[str] |  (optional)
    race = ['race_example'] # List[str] |  (optional)
    race_specify = ['race_specify_example'] # List[str] |  (optional)
    species = ['species_example'] # List[str] |  (optional)
    strain = ['strain_example'] # List[str] |  (optional)
    study_accession = ['study_accession_example'] # List[str] |  (optional)
    study_time_collected = 3.4 # float |  (optional)
    study_time_collected_gte = 3.4 # float |  (optional)
    study_time_collected_lte = 3.4 # float |  (optional)
    study_time_collected_gt = 3.4 # float |  (optional)
    study_time_collected_lt = 3.4 # float |  (optional)
    study_time_collected_unit = ['study_time_collected_unit_example'] # List[str] |  (optional)
    study_time_t0_event = ['study_time_t0_event_example'] # List[str] |  (optional)
    study_time_t0_event_specify = ['study_time_t0_event_specify_example'] # List[str] |  (optional)
    subject_accession = ['subject_accession_example'] # List[str] |  (optional)
    study_title = ['study_title_example'] # List[str] |  (optional)
    subject_phenotype = ['subject_phenotype_example'] # List[str] |  (optional)
    treatment_accession = ['treatment_accession_example'] # List[str] |  (optional)
    format = 'format_example' # str |  (optional)

    try:
        # Retrieve kIR Typing results using filters
        api_response = api_instance.get_kir_typing_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)
        print("The response of StudyResultApi->get_kir_typing_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_kir_typing_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **age_event** | [**List[str]**](str.md)|  | [optional] 
 **age_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **age_unit** | [**List[str]**](str.md)|  | [optional] 
 **ancestral_population** | [**List[str]**](str.md)|  | [optional] 
 **arm_accession** | [**List[str]**](str.md)|  | [optional] 
 **arm_name** | [**List[str]**](str.md)|  | [optional] 
 **biosample_accession** | [**List[str]**](str.md)|  | [optional] 
 **biosample_subtype** | [**List[str]**](str.md)|  | [optional] 
 **biosample_type** | [**List[str]**](str.md)|  | [optional] 
 **clinical** | **str**|  | [optional] 
 **ethnicity** | [**List[str]**](str.md)|  | [optional] 
 **experiment_accession** | [**List[str]**](str.md)|  | [optional] 
 **expsample_accession** | [**List[str]**](str.md)|  | [optional] 
 **gender** | [**List[str]**](str.md)|  | [optional] 
 **sex** | [**List[str]**](str.md)|  | [optional] 
 **max_subject_age** | **float**|  | [optional] 
 **max_subject_age_gte** | **float**|  | [optional] 
 **max_subject_age_lte** | **float**|  | [optional] 
 **max_subject_age_gt** | **float**|  | [optional] 
 **max_subject_age_lt** | **float**|  | [optional] 
 **min_subject_age** | **float**|  | [optional] 
 **min_subject_age_gte** | **float**|  | [optional] 
 **min_subject_age_lte** | **float**|  | [optional] 
 **min_subject_age_gt** | **float**|  | [optional] 
 **min_subject_age_lt** | **float**|  | [optional] 
 **measurement_technique** | [**List[str]**](str.md)|  | [optional] 
 **planned_visit_accession** | [**List[str]**](str.md)|  | [optional] 
 **race** | [**List[str]**](str.md)|  | [optional] 
 **race_specify** | [**List[str]**](str.md)|  | [optional] 
 **species** | [**List[str]**](str.md)|  | [optional] 
 **strain** | [**List[str]**](str.md)|  | [optional] 
 **study_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_time_collected** | **float**|  | [optional] 
 **study_time_collected_gte** | **float**|  | [optional] 
 **study_time_collected_lte** | **float**|  | [optional] 
 **study_time_collected_gt** | **float**|  | [optional] 
 **study_time_collected_lt** | **float**|  | [optional] 
 **study_time_collected_unit** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **subject_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_title** | [**List[str]**](str.md)|  | [optional] 
 **subject_phenotype** | [**List[str]**](str.md)|  | [optional] 
 **treatment_accession** | [**List[str]**](str.md)|  | [optional] 
 **format** | **str**|  | [optional] 

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
> List[MassSpectrometryResult] get_mass_spectrometry_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)

Retrieve Mass Spectrometry results using filters

Returns Mass Spectrometry results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
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
    age_event = ['age_event_example'] # List[str] |  (optional)
    age_event_specify = ['age_event_specify_example'] # List[str] |  (optional)
    age_unit = ['age_unit_example'] # List[str] |  (optional)
    ancestral_population = ['ancestral_population_example'] # List[str] |  (optional)
    arm_accession = ['arm_accession_example'] # List[str] |  (optional)
    arm_name = ['arm_name_example'] # List[str] |  (optional)
    biosample_accession = ['biosample_accession_example'] # List[str] |  (optional)
    biosample_subtype = ['biosample_subtype_example'] # List[str] |  (optional)
    biosample_type = ['biosample_type_example'] # List[str] |  (optional)
    clinical = 'clinical_example' # str |  (optional)
    ethnicity = ['ethnicity_example'] # List[str] |  (optional)
    experiment_accession = ['experiment_accession_example'] # List[str] |  (optional)
    expsample_accession = ['expsample_accession_example'] # List[str] |  (optional)
    gender = ['gender_example'] # List[str] |  (optional)
    sex = ['sex_example'] # List[str] |  (optional)
    max_subject_age = 3.4 # float |  (optional)
    max_subject_age_gte = 3.4 # float |  (optional)
    max_subject_age_lte = 3.4 # float |  (optional)
    max_subject_age_gt = 3.4 # float |  (optional)
    max_subject_age_lt = 3.4 # float |  (optional)
    min_subject_age = 3.4 # float |  (optional)
    min_subject_age_gte = 3.4 # float |  (optional)
    min_subject_age_lte = 3.4 # float |  (optional)
    min_subject_age_gt = 3.4 # float |  (optional)
    min_subject_age_lt = 3.4 # float |  (optional)
    measurement_technique = ['measurement_technique_example'] # List[str] |  (optional)
    planned_visit_accession = ['planned_visit_accession_example'] # List[str] |  (optional)
    race = ['race_example'] # List[str] |  (optional)
    race_specify = ['race_specify_example'] # List[str] |  (optional)
    species = ['species_example'] # List[str] |  (optional)
    strain = ['strain_example'] # List[str] |  (optional)
    study_accession = ['study_accession_example'] # List[str] |  (optional)
    study_time_collected = 3.4 # float |  (optional)
    study_time_collected_gte = 3.4 # float |  (optional)
    study_time_collected_lte = 3.4 # float |  (optional)
    study_time_collected_gt = 3.4 # float |  (optional)
    study_time_collected_lt = 3.4 # float |  (optional)
    study_time_collected_unit = ['study_time_collected_unit_example'] # List[str] |  (optional)
    study_time_t0_event = ['study_time_t0_event_example'] # List[str] |  (optional)
    study_time_t0_event_specify = ['study_time_t0_event_specify_example'] # List[str] |  (optional)
    subject_accession = ['subject_accession_example'] # List[str] |  (optional)
    study_title = ['study_title_example'] # List[str] |  (optional)
    subject_phenotype = ['subject_phenotype_example'] # List[str] |  (optional)
    treatment_accession = ['treatment_accession_example'] # List[str] |  (optional)
    format = 'format_example' # str |  (optional)

    try:
        # Retrieve Mass Spectrometry results using filters
        api_response = api_instance.get_mass_spectrometry_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)
        print("The response of StudyResultApi->get_mass_spectrometry_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_mass_spectrometry_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **age_event** | [**List[str]**](str.md)|  | [optional] 
 **age_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **age_unit** | [**List[str]**](str.md)|  | [optional] 
 **ancestral_population** | [**List[str]**](str.md)|  | [optional] 
 **arm_accession** | [**List[str]**](str.md)|  | [optional] 
 **arm_name** | [**List[str]**](str.md)|  | [optional] 
 **biosample_accession** | [**List[str]**](str.md)|  | [optional] 
 **biosample_subtype** | [**List[str]**](str.md)|  | [optional] 
 **biosample_type** | [**List[str]**](str.md)|  | [optional] 
 **clinical** | **str**|  | [optional] 
 **ethnicity** | [**List[str]**](str.md)|  | [optional] 
 **experiment_accession** | [**List[str]**](str.md)|  | [optional] 
 **expsample_accession** | [**List[str]**](str.md)|  | [optional] 
 **gender** | [**List[str]**](str.md)|  | [optional] 
 **sex** | [**List[str]**](str.md)|  | [optional] 
 **max_subject_age** | **float**|  | [optional] 
 **max_subject_age_gte** | **float**|  | [optional] 
 **max_subject_age_lte** | **float**|  | [optional] 
 **max_subject_age_gt** | **float**|  | [optional] 
 **max_subject_age_lt** | **float**|  | [optional] 
 **min_subject_age** | **float**|  | [optional] 
 **min_subject_age_gte** | **float**|  | [optional] 
 **min_subject_age_lte** | **float**|  | [optional] 
 **min_subject_age_gt** | **float**|  | [optional] 
 **min_subject_age_lt** | **float**|  | [optional] 
 **measurement_technique** | [**List[str]**](str.md)|  | [optional] 
 **planned_visit_accession** | [**List[str]**](str.md)|  | [optional] 
 **race** | [**List[str]**](str.md)|  | [optional] 
 **race_specify** | [**List[str]**](str.md)|  | [optional] 
 **species** | [**List[str]**](str.md)|  | [optional] 
 **strain** | [**List[str]**](str.md)|  | [optional] 
 **study_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_time_collected** | **float**|  | [optional] 
 **study_time_collected_gte** | **float**|  | [optional] 
 **study_time_collected_lte** | **float**|  | [optional] 
 **study_time_collected_gt** | **float**|  | [optional] 
 **study_time_collected_lt** | **float**|  | [optional] 
 **study_time_collected_unit** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **subject_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_title** | [**List[str]**](str.md)|  | [optional] 
 **subject_phenotype** | [**List[str]**](str.md)|  | [optional] 
 **treatment_accession** | [**List[str]**](str.md)|  | [optional] 
 **format** | **str**|  | [optional] 

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
> List[VMbaaResult] get_mbaa_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)

Retrieve MBAA results using filters

Returns MBAA results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
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
    age_event = ['age_event_example'] # List[str] |  (optional)
    age_event_specify = ['age_event_specify_example'] # List[str] |  (optional)
    age_unit = ['age_unit_example'] # List[str] |  (optional)
    ancestral_population = ['ancestral_population_example'] # List[str] |  (optional)
    arm_accession = ['arm_accession_example'] # List[str] |  (optional)
    arm_name = ['arm_name_example'] # List[str] |  (optional)
    biosample_accession = ['biosample_accession_example'] # List[str] |  (optional)
    biosample_subtype = ['biosample_subtype_example'] # List[str] |  (optional)
    biosample_type = ['biosample_type_example'] # List[str] |  (optional)
    clinical = 'clinical_example' # str |  (optional)
    ethnicity = ['ethnicity_example'] # List[str] |  (optional)
    experiment_accession = ['experiment_accession_example'] # List[str] |  (optional)
    expsample_accession = ['expsample_accession_example'] # List[str] |  (optional)
    gender = ['gender_example'] # List[str] |  (optional)
    sex = ['sex_example'] # List[str] |  (optional)
    max_subject_age = 3.4 # float |  (optional)
    max_subject_age_gte = 3.4 # float |  (optional)
    max_subject_age_lte = 3.4 # float |  (optional)
    max_subject_age_gt = 3.4 # float |  (optional)
    max_subject_age_lt = 3.4 # float |  (optional)
    min_subject_age = 3.4 # float |  (optional)
    min_subject_age_gte = 3.4 # float |  (optional)
    min_subject_age_lte = 3.4 # float |  (optional)
    min_subject_age_gt = 3.4 # float |  (optional)
    min_subject_age_lt = 3.4 # float |  (optional)
    measurement_technique = ['measurement_technique_example'] # List[str] |  (optional)
    planned_visit_accession = ['planned_visit_accession_example'] # List[str] |  (optional)
    race = ['race_example'] # List[str] |  (optional)
    race_specify = ['race_specify_example'] # List[str] |  (optional)
    species = ['species_example'] # List[str] |  (optional)
    strain = ['strain_example'] # List[str] |  (optional)
    study_accession = ['study_accession_example'] # List[str] |  (optional)
    study_time_collected = 3.4 # float |  (optional)
    study_time_collected_gte = 3.4 # float |  (optional)
    study_time_collected_lte = 3.4 # float |  (optional)
    study_time_collected_gt = 3.4 # float |  (optional)
    study_time_collected_lt = 3.4 # float |  (optional)
    study_time_collected_unit = ['study_time_collected_unit_example'] # List[str] |  (optional)
    study_time_t0_event = ['study_time_t0_event_example'] # List[str] |  (optional)
    study_time_t0_event_specify = ['study_time_t0_event_specify_example'] # List[str] |  (optional)
    subject_accession = ['subject_accession_example'] # List[str] |  (optional)
    study_title = ['study_title_example'] # List[str] |  (optional)
    subject_phenotype = ['subject_phenotype_example'] # List[str] |  (optional)
    treatment_accession = ['treatment_accession_example'] # List[str] |  (optional)
    format = 'format_example' # str |  (optional)

    try:
        # Retrieve MBAA results using filters
        api_response = api_instance.get_mbaa_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)
        print("The response of StudyResultApi->get_mbaa_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_mbaa_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **age_event** | [**List[str]**](str.md)|  | [optional] 
 **age_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **age_unit** | [**List[str]**](str.md)|  | [optional] 
 **ancestral_population** | [**List[str]**](str.md)|  | [optional] 
 **arm_accession** | [**List[str]**](str.md)|  | [optional] 
 **arm_name** | [**List[str]**](str.md)|  | [optional] 
 **biosample_accession** | [**List[str]**](str.md)|  | [optional] 
 **biosample_subtype** | [**List[str]**](str.md)|  | [optional] 
 **biosample_type** | [**List[str]**](str.md)|  | [optional] 
 **clinical** | **str**|  | [optional] 
 **ethnicity** | [**List[str]**](str.md)|  | [optional] 
 **experiment_accession** | [**List[str]**](str.md)|  | [optional] 
 **expsample_accession** | [**List[str]**](str.md)|  | [optional] 
 **gender** | [**List[str]**](str.md)|  | [optional] 
 **sex** | [**List[str]**](str.md)|  | [optional] 
 **max_subject_age** | **float**|  | [optional] 
 **max_subject_age_gte** | **float**|  | [optional] 
 **max_subject_age_lte** | **float**|  | [optional] 
 **max_subject_age_gt** | **float**|  | [optional] 
 **max_subject_age_lt** | **float**|  | [optional] 
 **min_subject_age** | **float**|  | [optional] 
 **min_subject_age_gte** | **float**|  | [optional] 
 **min_subject_age_lte** | **float**|  | [optional] 
 **min_subject_age_gt** | **float**|  | [optional] 
 **min_subject_age_lt** | **float**|  | [optional] 
 **measurement_technique** | [**List[str]**](str.md)|  | [optional] 
 **planned_visit_accession** | [**List[str]**](str.md)|  | [optional] 
 **race** | [**List[str]**](str.md)|  | [optional] 
 **race_specify** | [**List[str]**](str.md)|  | [optional] 
 **species** | [**List[str]**](str.md)|  | [optional] 
 **strain** | [**List[str]**](str.md)|  | [optional] 
 **study_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_time_collected** | **float**|  | [optional] 
 **study_time_collected_gte** | **float**|  | [optional] 
 **study_time_collected_lte** | **float**|  | [optional] 
 **study_time_collected_gt** | **float**|  | [optional] 
 **study_time_collected_lt** | **float**|  | [optional] 
 **study_time_collected_unit** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **subject_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_title** | [**List[str]**](str.md)|  | [optional] 
 **subject_phenotype** | [**List[str]**](str.md)|  | [optional] 
 **treatment_accession** | [**List[str]**](str.md)|  | [optional] 
 **format** | **str**|  | [optional] 

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
> List[VNeutAbTiterResult] get_neut_ab_titer_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)

Retrieve Neutralizing Antibody Titer results using filters

Returns Neutralizing Antibody Titer results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
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
    age_event = ['age_event_example'] # List[str] |  (optional)
    age_event_specify = ['age_event_specify_example'] # List[str] |  (optional)
    age_unit = ['age_unit_example'] # List[str] |  (optional)
    ancestral_population = ['ancestral_population_example'] # List[str] |  (optional)
    arm_accession = ['arm_accession_example'] # List[str] |  (optional)
    arm_name = ['arm_name_example'] # List[str] |  (optional)
    biosample_accession = ['biosample_accession_example'] # List[str] |  (optional)
    biosample_subtype = ['biosample_subtype_example'] # List[str] |  (optional)
    biosample_type = ['biosample_type_example'] # List[str] |  (optional)
    clinical = 'clinical_example' # str |  (optional)
    ethnicity = ['ethnicity_example'] # List[str] |  (optional)
    experiment_accession = ['experiment_accession_example'] # List[str] |  (optional)
    expsample_accession = ['expsample_accession_example'] # List[str] |  (optional)
    gender = ['gender_example'] # List[str] |  (optional)
    sex = ['sex_example'] # List[str] |  (optional)
    max_subject_age = 3.4 # float |  (optional)
    max_subject_age_gte = 3.4 # float |  (optional)
    max_subject_age_lte = 3.4 # float |  (optional)
    max_subject_age_gt = 3.4 # float |  (optional)
    max_subject_age_lt = 3.4 # float |  (optional)
    min_subject_age = 3.4 # float |  (optional)
    min_subject_age_gte = 3.4 # float |  (optional)
    min_subject_age_lte = 3.4 # float |  (optional)
    min_subject_age_gt = 3.4 # float |  (optional)
    min_subject_age_lt = 3.4 # float |  (optional)
    measurement_technique = ['measurement_technique_example'] # List[str] |  (optional)
    planned_visit_accession = ['planned_visit_accession_example'] # List[str] |  (optional)
    race = ['race_example'] # List[str] |  (optional)
    race_specify = ['race_specify_example'] # List[str] |  (optional)
    species = ['species_example'] # List[str] |  (optional)
    strain = ['strain_example'] # List[str] |  (optional)
    study_accession = ['study_accession_example'] # List[str] |  (optional)
    study_time_collected = 3.4 # float |  (optional)
    study_time_collected_gte = 3.4 # float |  (optional)
    study_time_collected_lte = 3.4 # float |  (optional)
    study_time_collected_gt = 3.4 # float |  (optional)
    study_time_collected_lt = 3.4 # float |  (optional)
    study_time_collected_unit = ['study_time_collected_unit_example'] # List[str] |  (optional)
    study_time_t0_event = ['study_time_t0_event_example'] # List[str] |  (optional)
    study_time_t0_event_specify = ['study_time_t0_event_specify_example'] # List[str] |  (optional)
    subject_accession = ['subject_accession_example'] # List[str] |  (optional)
    study_title = ['study_title_example'] # List[str] |  (optional)
    subject_phenotype = ['subject_phenotype_example'] # List[str] |  (optional)
    treatment_accession = ['treatment_accession_example'] # List[str] |  (optional)
    format = 'format_example' # str |  (optional)

    try:
        # Retrieve Neutralizing Antibody Titer results using filters
        api_response = api_instance.get_neut_ab_titer_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)
        print("The response of StudyResultApi->get_neut_ab_titer_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_neut_ab_titer_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **age_event** | [**List[str]**](str.md)|  | [optional] 
 **age_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **age_unit** | [**List[str]**](str.md)|  | [optional] 
 **ancestral_population** | [**List[str]**](str.md)|  | [optional] 
 **arm_accession** | [**List[str]**](str.md)|  | [optional] 
 **arm_name** | [**List[str]**](str.md)|  | [optional] 
 **biosample_accession** | [**List[str]**](str.md)|  | [optional] 
 **biosample_subtype** | [**List[str]**](str.md)|  | [optional] 
 **biosample_type** | [**List[str]**](str.md)|  | [optional] 
 **clinical** | **str**|  | [optional] 
 **ethnicity** | [**List[str]**](str.md)|  | [optional] 
 **experiment_accession** | [**List[str]**](str.md)|  | [optional] 
 **expsample_accession** | [**List[str]**](str.md)|  | [optional] 
 **gender** | [**List[str]**](str.md)|  | [optional] 
 **sex** | [**List[str]**](str.md)|  | [optional] 
 **max_subject_age** | **float**|  | [optional] 
 **max_subject_age_gte** | **float**|  | [optional] 
 **max_subject_age_lte** | **float**|  | [optional] 
 **max_subject_age_gt** | **float**|  | [optional] 
 **max_subject_age_lt** | **float**|  | [optional] 
 **min_subject_age** | **float**|  | [optional] 
 **min_subject_age_gte** | **float**|  | [optional] 
 **min_subject_age_lte** | **float**|  | [optional] 
 **min_subject_age_gt** | **float**|  | [optional] 
 **min_subject_age_lt** | **float**|  | [optional] 
 **measurement_technique** | [**List[str]**](str.md)|  | [optional] 
 **planned_visit_accession** | [**List[str]**](str.md)|  | [optional] 
 **race** | [**List[str]**](str.md)|  | [optional] 
 **race_specify** | [**List[str]**](str.md)|  | [optional] 
 **species** | [**List[str]**](str.md)|  | [optional] 
 **strain** | [**List[str]**](str.md)|  | [optional] 
 **study_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_time_collected** | **float**|  | [optional] 
 **study_time_collected_gte** | **float**|  | [optional] 
 **study_time_collected_lte** | **float**|  | [optional] 
 **study_time_collected_gt** | **float**|  | [optional] 
 **study_time_collected_lt** | **float**|  | [optional] 
 **study_time_collected_unit** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **subject_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_title** | [**List[str]**](str.md)|  | [optional] 
 **subject_phenotype** | [**List[str]**](str.md)|  | [optional] 
 **treatment_accession** | [**List[str]**](str.md)|  | [optional] 
 **format** | **str**|  | [optional] 

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
> List[VPcrResult] get_pcr_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)

Retrieve PCR results using filters

Returns PCR results based on filter criteria

### Example

* OAuth Authentication (immport-security):

```python
import immport_client
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
    age_event = ['age_event_example'] # List[str] |  (optional)
    age_event_specify = ['age_event_specify_example'] # List[str] |  (optional)
    age_unit = ['age_unit_example'] # List[str] |  (optional)
    ancestral_population = ['ancestral_population_example'] # List[str] |  (optional)
    arm_accession = ['arm_accession_example'] # List[str] |  (optional)
    arm_name = ['arm_name_example'] # List[str] |  (optional)
    biosample_accession = ['biosample_accession_example'] # List[str] |  (optional)
    biosample_subtype = ['biosample_subtype_example'] # List[str] |  (optional)
    biosample_type = ['biosample_type_example'] # List[str] |  (optional)
    clinical = 'clinical_example' # str |  (optional)
    ethnicity = ['ethnicity_example'] # List[str] |  (optional)
    experiment_accession = ['experiment_accession_example'] # List[str] |  (optional)
    expsample_accession = ['expsample_accession_example'] # List[str] |  (optional)
    gender = ['gender_example'] # List[str] |  (optional)
    sex = ['sex_example'] # List[str] |  (optional)
    max_subject_age = 3.4 # float |  (optional)
    max_subject_age_gte = 3.4 # float |  (optional)
    max_subject_age_lte = 3.4 # float |  (optional)
    max_subject_age_gt = 3.4 # float |  (optional)
    max_subject_age_lt = 3.4 # float |  (optional)
    min_subject_age = 3.4 # float |  (optional)
    min_subject_age_gte = 3.4 # float |  (optional)
    min_subject_age_lte = 3.4 # float |  (optional)
    min_subject_age_gt = 3.4 # float |  (optional)
    min_subject_age_lt = 3.4 # float |  (optional)
    measurement_technique = ['measurement_technique_example'] # List[str] |  (optional)
    planned_visit_accession = ['planned_visit_accession_example'] # List[str] |  (optional)
    race = ['race_example'] # List[str] |  (optional)
    race_specify = ['race_specify_example'] # List[str] |  (optional)
    species = ['species_example'] # List[str] |  (optional)
    strain = ['strain_example'] # List[str] |  (optional)
    study_accession = ['study_accession_example'] # List[str] |  (optional)
    study_time_collected = 3.4 # float |  (optional)
    study_time_collected_gte = 3.4 # float |  (optional)
    study_time_collected_lte = 3.4 # float |  (optional)
    study_time_collected_gt = 3.4 # float |  (optional)
    study_time_collected_lt = 3.4 # float |  (optional)
    study_time_collected_unit = ['study_time_collected_unit_example'] # List[str] |  (optional)
    study_time_t0_event = ['study_time_t0_event_example'] # List[str] |  (optional)
    study_time_t0_event_specify = ['study_time_t0_event_specify_example'] # List[str] |  (optional)
    subject_accession = ['subject_accession_example'] # List[str] |  (optional)
    study_title = ['study_title_example'] # List[str] |  (optional)
    subject_phenotype = ['subject_phenotype_example'] # List[str] |  (optional)
    treatment_accession = ['treatment_accession_example'] # List[str] |  (optional)
    format = 'format_example' # str |  (optional)

    try:
        # Retrieve PCR results using filters
        api_response = api_instance.get_pcr_result(age_event=age_event, age_event_specify=age_event_specify, age_unit=age_unit, ancestral_population=ancestral_population, arm_accession=arm_accession, arm_name=arm_name, biosample_accession=biosample_accession, biosample_subtype=biosample_subtype, biosample_type=biosample_type, clinical=clinical, ethnicity=ethnicity, experiment_accession=experiment_accession, expsample_accession=expsample_accession, gender=gender, sex=sex, max_subject_age=max_subject_age, max_subject_age_gte=max_subject_age_gte, max_subject_age_lte=max_subject_age_lte, max_subject_age_gt=max_subject_age_gt, max_subject_age_lt=max_subject_age_lt, min_subject_age=min_subject_age, min_subject_age_gte=min_subject_age_gte, min_subject_age_lte=min_subject_age_lte, min_subject_age_gt=min_subject_age_gt, min_subject_age_lt=min_subject_age_lt, measurement_technique=measurement_technique, planned_visit_accession=planned_visit_accession, race=race, race_specify=race_specify, species=species, strain=strain, study_accession=study_accession, study_time_collected=study_time_collected, study_time_collected_gte=study_time_collected_gte, study_time_collected_lte=study_time_collected_lte, study_time_collected_gt=study_time_collected_gt, study_time_collected_lt=study_time_collected_lt, study_time_collected_unit=study_time_collected_unit, study_time_t0_event=study_time_t0_event, study_time_t0_event_specify=study_time_t0_event_specify, subject_accession=subject_accession, study_title=study_title, subject_phenotype=subject_phenotype, treatment_accession=treatment_accession, format=format)
        print("The response of StudyResultApi->get_pcr_result:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudyResultApi->get_pcr_result: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **age_event** | [**List[str]**](str.md)|  | [optional] 
 **age_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **age_unit** | [**List[str]**](str.md)|  | [optional] 
 **ancestral_population** | [**List[str]**](str.md)|  | [optional] 
 **arm_accession** | [**List[str]**](str.md)|  | [optional] 
 **arm_name** | [**List[str]**](str.md)|  | [optional] 
 **biosample_accession** | [**List[str]**](str.md)|  | [optional] 
 **biosample_subtype** | [**List[str]**](str.md)|  | [optional] 
 **biosample_type** | [**List[str]**](str.md)|  | [optional] 
 **clinical** | **str**|  | [optional] 
 **ethnicity** | [**List[str]**](str.md)|  | [optional] 
 **experiment_accession** | [**List[str]**](str.md)|  | [optional] 
 **expsample_accession** | [**List[str]**](str.md)|  | [optional] 
 **gender** | [**List[str]**](str.md)|  | [optional] 
 **sex** | [**List[str]**](str.md)|  | [optional] 
 **max_subject_age** | **float**|  | [optional] 
 **max_subject_age_gte** | **float**|  | [optional] 
 **max_subject_age_lte** | **float**|  | [optional] 
 **max_subject_age_gt** | **float**|  | [optional] 
 **max_subject_age_lt** | **float**|  | [optional] 
 **min_subject_age** | **float**|  | [optional] 
 **min_subject_age_gte** | **float**|  | [optional] 
 **min_subject_age_lte** | **float**|  | [optional] 
 **min_subject_age_gt** | **float**|  | [optional] 
 **min_subject_age_lt** | **float**|  | [optional] 
 **measurement_technique** | [**List[str]**](str.md)|  | [optional] 
 **planned_visit_accession** | [**List[str]**](str.md)|  | [optional] 
 **race** | [**List[str]**](str.md)|  | [optional] 
 **race_specify** | [**List[str]**](str.md)|  | [optional] 
 **species** | [**List[str]**](str.md)|  | [optional] 
 **strain** | [**List[str]**](str.md)|  | [optional] 
 **study_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_time_collected** | **float**|  | [optional] 
 **study_time_collected_gte** | **float**|  | [optional] 
 **study_time_collected_lte** | **float**|  | [optional] 
 **study_time_collected_gt** | **float**|  | [optional] 
 **study_time_collected_lt** | **float**|  | [optional] 
 **study_time_collected_unit** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event** | [**List[str]**](str.md)|  | [optional] 
 **study_time_t0_event_specify** | [**List[str]**](str.md)|  | [optional] 
 **subject_accession** | [**List[str]**](str.md)|  | [optional] 
 **study_title** | [**List[str]**](str.md)|  | [optional] 
 **subject_phenotype** | [**List[str]**](str.md)|  | [optional] 
 **treatment_accession** | [**List[str]**](str.md)|  | [optional] 
 **format** | **str**|  | [optional] 

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

