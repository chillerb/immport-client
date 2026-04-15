# immport_client.StudySearchApi

All URIs are relative to *https://immport.org/data/query*

Method | HTTP request | Description
------------- | ------------- | -------------
[**study_search**](StudySearchApi.md#study_search) | **GET** /api/search/study | Search studies
[**subject_search**](StudySearchApi.md#subject_search) | **GET** /api/search/subject | Search subjects


# **study_search**
> object study_search(term=term, from_record=from_record, page_size=page_size, pre_tag=pre_tag, post_tag=post_tag, format=format, source_fields=source_fields, sort_field=sort_field, sort_field_direction=sort_field_direction, search_fields=search_fields, study_accession=study_accession, subject_accession=subject_accession, program_name=program_name, condition_or_disease=condition_or_disease, research_focus=research_focus, clinical_trial=clinical_trial, sex=sex, race=race, ethnicity=ethnicity, species=species, min_age=min_age, age_range=age_range, assay_method=assay_method, biosample_type=biosample_type, has_assessment=has_assessment, has_lab_test=has_lab_test)

Search studies

Searches studies using a full-text term and/or facet filters.

- All fields in the Parameters are sent as **query parameters**.
- Multi-value filters can be repeated: conditionOrDisease=asthma&conditionOrDisease=influenza
  (or comma-separated depending on your binding expectations like conditionOrDisease=asthma,influenza).


### Example


```python
import immport_client
from immport_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://immport.org/data/query
# See configuration.py for a list of all supported configuration parameters.
configuration = immport_client.Configuration(
    host = "https://immport.org/data/query"
)


# Enter a context with an instance of the API client
with immport_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = immport_client.StudySearchApi(api_client)
    term = 'term_example' # str |     Full-text search term supporting partial matching. Searches within words by default ('flu' finds 'influenza'). Use quotes for exact phrases (\\\"influenza vaccine\\\" finds only that exact phrase).<br>     **Example:** influenza vaccine   (optional)
    from_record = '0' # str | Zero-based pagination offset (starting record index)  (optional) (default to '0')
    page_size = '10' # str | Maximum number of records to return per page (optional) (default to '10')
    pre_tag = '<em>' # str | HTML tag to prepend to highlighted search terms in results (optional)
    post_tag = '</em>' # str | HTML tag to append to highlighted search terms in results (optional)
    format = json # str | Response format type (optional) (default to json)
    source_fields = 'source_fields_example' # str | Comma-separated list of specific fields to include in the return response.  ### Study Fields - **study_accession** : PID for the study - **actual_enrollment** : Number of subjects enrolled in the study - **age_range** : age range of the participants involved in the study - **analyte_preferred_count** : The total number of distinct preferred analytes associated with a study. An analyte is a biological substance measured in an assay - **assay_method_count** : The total number of distinct assay methods (measurement techniques) associated with a study. - **assessment_panel_count** : Assesment Panel is collection of assessments which are evaluations ( CRS, questionaires, ratings based on a reference scale) of subjects that do not involve drawing a sample from a subject. The number of the Assessment Panel's in this study - **brief_title** : Short title for the study or trial - **condition_or_disease** : The condition(s)/disease(s) that is (are) being researched or evaluated in the study. - **contract_grant_external_id** : ID from funding source - **contract_grant_name** : Name of the Contract or grant that funded the research. - **doi** : Digital object identifier (DOI) is a type of persistent identifier used to uniquely identify objects. DOI used for the study. - **sex_included** : Indicates the biological sex categories represented among study subjects. - **initial_data_release_date** : Initial date study shared - **initial_data_release_version_number** : Initial version of study shared - **lab_test_panel_count** : Lab Test Panel is a collection of Lab Tests. The number of the Lab Test Panel's in this study - **latest_data_release_version_number** : Latest version of study shared - **latest_data_release_date** : Latest date when the study was shared - **min_age** : The subject age at the outset of the study may be determined form one of several study milestones as indicated in the Age Event column. - **max_age** : The subject age at the end of the study may be determined form one of several study milestones. - **planned_visit_total_count** : Planned Visit describes a STUDY indicated encounter with a SUBJECT. Total number of planned visit in this study - **program_name** : Programs are the NIH organizational basis for administering grants and contracts. - **pubmed_id** : The Pubmed or PubMedCentral identifier of an article that includes data from this study. - **research_focus** : Describes a study's focus, purpose or category. - **shared_subject_count** : The number od participants in the study that have been shared. - **species** : Represents the organism associated with the study or subjects - **study_pi** : The name of the Principal Investigator (PI) responsible for the study.  ### Subject Fields - **study_accession** : PID for the study - **subject_accession** : PID for the subject participant - **arm_name** : The name of the study's arm(s) or cohort(s) group subjects by criteria relevant to the study (e.g. age, condition) and/or treatments or interventions. - **assay_method** : The experimental or laboratory technique used to measure, detect, or quantify biological molecules, cells, or other analytes in a study. - **biosample_type** : The sample types are adopted from Uberon, Cell and CHEBI ontologies. - **clinical_trial** : Indicates if the study is a clinical trial study - **condition_or_disease** : Reported medical conditions or diseases investigated in the study - **ethnicity** : Particpant ethnicity - **sex** : Particpant sex - **has_assessment** : Indicates if the study includes assessment data. Assessment data are evaluations ( CRS, questionaires, ratings based on a reference scale) of subjects that do not involve drawing a sample from a subject. - **has_lab_test** : Indicates if the study includes laboratory test results. Lab Test are laboratory process operating on a biological sample that produces a single value. Similar to an EXPERIMENT, but with a clinical assay focus. - **min_age** : The subject age at the outset of the study may be determined form one of several study milestones as indicated in the Age Event column. - **race** : Particpant race - **research_focus** : Describes a study's focus, purpose or category. - **species** : Represents the organism associated with the study or subjects  **Example:** study_accession,condition_or_disease,brief_title  (optional)
    sort_field = 'sort_field_example' # str | Field name used to sort results.  ### Study Sort Fields - study_accession - actual_enrollment - brief_-  ** - condition_or_disease - contract_grant_name - contract_grant_external_id - doi - sex_included - latest_data_release_version_number - latest_data_release_date - min_age - program_name - pubmed_id - research_focus - species - study_pi  ### Subject Sort Fields - study_accession - subject_accession - arm_name - assay_method - biosample_type - clinical_trial - condition_or_disease - ethnicity - sex - has_assessment - has_lab_test - min_age - race - research_focus - species  **Example:** study_accession  (optional)
    sort_field_direction = asc # str | Sort order direction (optional) (default to asc)
    search_fields = 'search_fields_example' # str | List of specific fields to search within (limits search scope to specified fields). Accepts multiple values comma separated. (optional)
    study_accession = 'study_accession_example' # str | Filter by specific study accession identifier(s). This is the persistant identifier for the study. Accepts multiple values comma separated.  **Example:**   SDY1,SDY2  (optional)
    subject_accession = 'subject_accession_example' # str | Filter by specific subject accession identifier(s). This is the persistant identifier for the subject. Accepts multiple values comma separated. **Example:** SUB00240,SUB00254  (optional)
    program_name = 'program_name_example' # str | Filter by program name(s). Programs are the NIH organizational basis for administering grants and contracts. Accepts multiple values comma separated.   **Example:**   SeroNet,Asthma and Allergic Diseases Cooperative Research Centers (AADCRC) RFA-AI-12-006  (optional)
    condition_or_disease = 'asthma,COVID-19' # str | Filters results to studies/subjects associated with one or more reported medical conditions or diseases investigated in the study. Accepts multiple values comma separated.  Lookup values can be retrieved from: [Disease Lookup API](https://www.immport.org/data/query/api/lookup/lkDisease?format=json)  (optional)
    research_focus = 'research_focus_example' # str |   Filter by research focus area(s). Describes a study's focus, purpose or category. Accepts multiple values comma separated.    Lookup values can be retrieved from:   [Research Focus Lookup API](https://www.immport.org/data/query/api/lookup/lkResearchFocus?format=json)    **Example:** Transplantation,Vaccine Response  (optional)
    clinical_trial = 'clinical_trial_example' # str | Filter to include only clinical trials : Y or N. Accepts multiple values comma separated. (optional)
    sex = 'sex_example' # str |   Filter by participant biological sex(s). Accepts multiple values comma separated.    Lookup values can be retrieved from:   [Sex Lookup API](https://www.immport.org/data/query/api/lookup/lkSex?format=json)    **Example:** Female   (optional)
    race = 'race_example' # str |   Filter by subject race. Accepts multiple values comma separated. Controlled vocabulary for Race follows the census designation and OMB Directive 15.    Lookup values can be retrieved from:   [Race Lookup API](https://www.immport.org/data/query/api/lookup/lkRace?format=json)    **Example:** Asian, White   (optional)
    ethnicity = 'ethnicity_example' # str | Filter by subject ethnicity. Accepts multiple values comma separated. Controlled vocabulary for Ethnicity follows the census designation and OMB Directive 15.  Lookup values can be retrieved from: [Ethnicity Lookup API](https://www.immport.org/data/query/api/lookup/lkSampleType?format=json)   **Example:**  Hispanic or Latino  (optional)
    species = 'species_example' # str | Filter by species studied. Accepts multiple values comma separated. Represents the organism associated with the study or subjects          (e.g., Homo sapiens, Mus musculus).  Lookup values can be retrieved from: [Species Lookup API](https://www.immport.org/data/query/api/lookup/lkSpecies?format=json)   **Example:**     Homo sapiens, Mus musculus  (optional)
    min_age = 'min_age_example' # str | Minimum age of study participants (optional)
    age_range = 'age_range_example' # str | Age range of study participants (e.g., '18-65') (optional)
    assay_method = 'assay_method_example' # str | Filter by assay method(s) used in the study. Accepts multiple values comma separated.  Represents the experimental measurement techniques applied to generate study data (e.g., Flow Cytometry, ELISA, ELISPOT).  Lookup values can be retrieved from: [Assay Method Lookup API](https://www.immport.org/data/query/api/lookup/lkExpMeasurementTech?format=json)   **Example:**     Flow Cytometry, ELISA, ELISPOT  (optional)
    biosample_type = 'biosample_type_example' # str | Filter by biological sample type(s) collected. Accepts multiple values comma separated.  Represents the type of biospecimen obtained from subjects for analysis  Lookup values can be retrieved from: [Biological Sample Type Lookup API](https://www.immport.org/data/query/api/lookup/lkSampleType?format=json)  **Example:** Bone, Cord blood  (optional)
    has_assessment = 'has_assessment_example' # str | Facet filter indicating whether the study includes assessment data.  Evaluations ( CRS, questionaires, ratings based on a reference scale) of subjects that do not involve drawing a sample from a subject.  Accepts one or more of the following values: Y = Includes assessment data N = Does not include assessment data  Multiple values match any of the provided options.  (optional)
    has_lab_test = 'has_lab_test_example' # str | Facet filter indicating whether the study includes laboratory test results.  Laboratory process operating on a biological sample that produces a single value. Similar to an EXPERIMENT, but with a clinical assay focus.  Accepts one or more of the following values: Y = Includes laboratory test results N = Does not include laboratory test results  Multiple values match any of the provided options.  (optional)

    try:
        # Search studies
        api_response = api_instance.study_search(term=term, from_record=from_record, page_size=page_size, pre_tag=pre_tag, post_tag=post_tag, format=format, source_fields=source_fields, sort_field=sort_field, sort_field_direction=sort_field_direction, search_fields=search_fields, study_accession=study_accession, subject_accession=subject_accession, program_name=program_name, condition_or_disease=condition_or_disease, research_focus=research_focus, clinical_trial=clinical_trial, sex=sex, race=race, ethnicity=ethnicity, species=species, min_age=min_age, age_range=age_range, assay_method=assay_method, biosample_type=biosample_type, has_assessment=has_assessment, has_lab_test=has_lab_test)
        print("The response of StudySearchApi->study_search:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudySearchApi->study_search: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **term** | **str**|     Full-text search term supporting partial matching. Searches within words by default (&#39;flu&#39; finds &#39;influenza&#39;). Use quotes for exact phrases (\\\&quot;influenza vaccine\\\&quot; finds only that exact phrase).&lt;br&gt;     **Example:** influenza vaccine   | [optional] 
 **from_record** | **str**| Zero-based pagination offset (starting record index)  | [optional] [default to &#39;0&#39;]
 **page_size** | **str**| Maximum number of records to return per page | [optional] [default to &#39;10&#39;]
 **pre_tag** | **str**| HTML tag to prepend to highlighted search terms in results | [optional] 
 **post_tag** | **str**| HTML tag to append to highlighted search terms in results | [optional] 
 **format** | **str**| Response format type | [optional] [default to json]
 **source_fields** | **str**| Comma-separated list of specific fields to include in the return response.  ### Study Fields - **study_accession** : PID for the study - **actual_enrollment** : Number of subjects enrolled in the study - **age_range** : age range of the participants involved in the study - **analyte_preferred_count** : The total number of distinct preferred analytes associated with a study. An analyte is a biological substance measured in an assay - **assay_method_count** : The total number of distinct assay methods (measurement techniques) associated with a study. - **assessment_panel_count** : Assesment Panel is collection of assessments which are evaluations ( CRS, questionaires, ratings based on a reference scale) of subjects that do not involve drawing a sample from a subject. The number of the Assessment Panel&#39;s in this study - **brief_title** : Short title for the study or trial - **condition_or_disease** : The condition(s)/disease(s) that is (are) being researched or evaluated in the study. - **contract_grant_external_id** : ID from funding source - **contract_grant_name** : Name of the Contract or grant that funded the research. - **doi** : Digital object identifier (DOI) is a type of persistent identifier used to uniquely identify objects. DOI used for the study. - **sex_included** : Indicates the biological sex categories represented among study subjects. - **initial_data_release_date** : Initial date study shared - **initial_data_release_version_number** : Initial version of study shared - **lab_test_panel_count** : Lab Test Panel is a collection of Lab Tests. The number of the Lab Test Panel&#39;s in this study - **latest_data_release_version_number** : Latest version of study shared - **latest_data_release_date** : Latest date when the study was shared - **min_age** : The subject age at the outset of the study may be determined form one of several study milestones as indicated in the Age Event column. - **max_age** : The subject age at the end of the study may be determined form one of several study milestones. - **planned_visit_total_count** : Planned Visit describes a STUDY indicated encounter with a SUBJECT. Total number of planned visit in this study - **program_name** : Programs are the NIH organizational basis for administering grants and contracts. - **pubmed_id** : The Pubmed or PubMedCentral identifier of an article that includes data from this study. - **research_focus** : Describes a study&#39;s focus, purpose or category. - **shared_subject_count** : The number od participants in the study that have been shared. - **species** : Represents the organism associated with the study or subjects - **study_pi** : The name of the Principal Investigator (PI) responsible for the study.  ### Subject Fields - **study_accession** : PID for the study - **subject_accession** : PID for the subject participant - **arm_name** : The name of the study&#39;s arm(s) or cohort(s) group subjects by criteria relevant to the study (e.g. age, condition) and/or treatments or interventions. - **assay_method** : The experimental or laboratory technique used to measure, detect, or quantify biological molecules, cells, or other analytes in a study. - **biosample_type** : The sample types are adopted from Uberon, Cell and CHEBI ontologies. - **clinical_trial** : Indicates if the study is a clinical trial study - **condition_or_disease** : Reported medical conditions or diseases investigated in the study - **ethnicity** : Particpant ethnicity - **sex** : Particpant sex - **has_assessment** : Indicates if the study includes assessment data. Assessment data are evaluations ( CRS, questionaires, ratings based on a reference scale) of subjects that do not involve drawing a sample from a subject. - **has_lab_test** : Indicates if the study includes laboratory test results. Lab Test are laboratory process operating on a biological sample that produces a single value. Similar to an EXPERIMENT, but with a clinical assay focus. - **min_age** : The subject age at the outset of the study may be determined form one of several study milestones as indicated in the Age Event column. - **race** : Particpant race - **research_focus** : Describes a study&#39;s focus, purpose or category. - **species** : Represents the organism associated with the study or subjects  **Example:** study_accession,condition_or_disease,brief_title  | [optional] 
 **sort_field** | **str**| Field name used to sort results.  ### Study Sort Fields - study_accession - actual_enrollment - brief_-  ** - condition_or_disease - contract_grant_name - contract_grant_external_id - doi - sex_included - latest_data_release_version_number - latest_data_release_date - min_age - program_name - pubmed_id - research_focus - species - study_pi  ### Subject Sort Fields - study_accession - subject_accession - arm_name - assay_method - biosample_type - clinical_trial - condition_or_disease - ethnicity - sex - has_assessment - has_lab_test - min_age - race - research_focus - species  **Example:** study_accession  | [optional] 
 **sort_field_direction** | **str**| Sort order direction | [optional] [default to asc]
 **search_fields** | **str**| List of specific fields to search within (limits search scope to specified fields). Accepts multiple values comma separated. | [optional] 
 **study_accession** | **str**| Filter by specific study accession identifier(s). This is the persistant identifier for the study. Accepts multiple values comma separated.  **Example:**   SDY1,SDY2  | [optional] 
 **subject_accession** | **str**| Filter by specific subject accession identifier(s). This is the persistant identifier for the subject. Accepts multiple values comma separated. **Example:** SUB00240,SUB00254  | [optional] 
 **program_name** | **str**| Filter by program name(s). Programs are the NIH organizational basis for administering grants and contracts. Accepts multiple values comma separated.   **Example:**   SeroNet,Asthma and Allergic Diseases Cooperative Research Centers (AADCRC) RFA-AI-12-006  | [optional] 
 **condition_or_disease** | **str**| Filters results to studies/subjects associated with one or more reported medical conditions or diseases investigated in the study. Accepts multiple values comma separated.  Lookup values can be retrieved from: [Disease Lookup API](https://www.immport.org/data/query/api/lookup/lkDisease?format&#x3D;json)  | [optional] 
 **research_focus** | **str**|   Filter by research focus area(s). Describes a study&#39;s focus, purpose or category. Accepts multiple values comma separated.    Lookup values can be retrieved from:   [Research Focus Lookup API](https://www.immport.org/data/query/api/lookup/lkResearchFocus?format&#x3D;json)    **Example:** Transplantation,Vaccine Response  | [optional] 
 **clinical_trial** | **str**| Filter to include only clinical trials : Y or N. Accepts multiple values comma separated. | [optional] 
 **sex** | **str**|   Filter by participant biological sex(s). Accepts multiple values comma separated.    Lookup values can be retrieved from:   [Sex Lookup API](https://www.immport.org/data/query/api/lookup/lkSex?format&#x3D;json)    **Example:** Female   | [optional] 
 **race** | **str**|   Filter by subject race. Accepts multiple values comma separated. Controlled vocabulary for Race follows the census designation and OMB Directive 15.    Lookup values can be retrieved from:   [Race Lookup API](https://www.immport.org/data/query/api/lookup/lkRace?format&#x3D;json)    **Example:** Asian, White   | [optional] 
 **ethnicity** | **str**| Filter by subject ethnicity. Accepts multiple values comma separated. Controlled vocabulary for Ethnicity follows the census designation and OMB Directive 15.  Lookup values can be retrieved from: [Ethnicity Lookup API](https://www.immport.org/data/query/api/lookup/lkSampleType?format&#x3D;json)   **Example:**  Hispanic or Latino  | [optional] 
 **species** | **str**| Filter by species studied. Accepts multiple values comma separated. Represents the organism associated with the study or subjects          (e.g., Homo sapiens, Mus musculus).  Lookup values can be retrieved from: [Species Lookup API](https://www.immport.org/data/query/api/lookup/lkSpecies?format&#x3D;json)   **Example:**     Homo sapiens, Mus musculus  | [optional] 
 **min_age** | **str**| Minimum age of study participants | [optional] 
 **age_range** | **str**| Age range of study participants (e.g., &#39;18-65&#39;) | [optional] 
 **assay_method** | **str**| Filter by assay method(s) used in the study. Accepts multiple values comma separated.  Represents the experimental measurement techniques applied to generate study data (e.g., Flow Cytometry, ELISA, ELISPOT).  Lookup values can be retrieved from: [Assay Method Lookup API](https://www.immport.org/data/query/api/lookup/lkExpMeasurementTech?format&#x3D;json)   **Example:**     Flow Cytometry, ELISA, ELISPOT  | [optional] 
 **biosample_type** | **str**| Filter by biological sample type(s) collected. Accepts multiple values comma separated.  Represents the type of biospecimen obtained from subjects for analysis  Lookup values can be retrieved from: [Biological Sample Type Lookup API](https://www.immport.org/data/query/api/lookup/lkSampleType?format&#x3D;json)  **Example:** Bone, Cord blood  | [optional] 
 **has_assessment** | **str**| Facet filter indicating whether the study includes assessment data.  Evaluations ( CRS, questionaires, ratings based on a reference scale) of subjects that do not involve drawing a sample from a subject.  Accepts one or more of the following values: Y &#x3D; Includes assessment data N &#x3D; Does not include assessment data  Multiple values match any of the provided options.  | [optional] 
 **has_lab_test** | **str**| Facet filter indicating whether the study includes laboratory test results.  Laboratory process operating on a biological sample that produces a single value. Similar to an EXPERIMENT, but with a clinical assay focus.  Accepts one or more of the following values: Y &#x3D; Includes laboratory test results N &#x3D; Does not include laboratory test results  Multiple values match any of the provided options.  | [optional] 

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**401** | Unauthorized (missing/invalid token). |  -  |
**200** | Search results returned successfully. |  -  |
**400** | Invalid query parameters. |  -  |
**403** | Forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **subject_search**
> object subject_search(term=term, from_record=from_record, page_size=page_size, pre_tag=pre_tag, post_tag=post_tag, format=format, source_fields=source_fields, sort_field=sort_field, sort_field_direction=sort_field_direction, search_fields=search_fields, study_accession=study_accession, subject_accession=subject_accession, program_name=program_name, condition_or_disease=condition_or_disease, research_focus=research_focus, clinical_trial=clinical_trial, sex=sex, race=race, ethnicity=ethnicity, species=species, min_age=min_age, age_range=age_range, assay_method=assay_method, biosample_type=biosample_type, has_assessment=has_assessment, has_lab_test=has_lab_test)

Search subjects

Searches subjects using a full-text term and/or facet filters.

- All fields in the Parameters are sent as **query parameters**.
- Multi-value filters can be repeated: conditionOrDisease=asthma&conditionOrDisease=influenza
  (or comma-separated depending on your binding expectations like conditionOrDisease=asthma,influenza).


### Example


```python
import immport_client
from immport_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://immport.org/data/query
# See configuration.py for a list of all supported configuration parameters.
configuration = immport_client.Configuration(
    host = "https://immport.org/data/query"
)


# Enter a context with an instance of the API client
with immport_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = immport_client.StudySearchApi(api_client)
    term = 'term_example' # str |     Full-text search term supporting partial matching. Searches within words by default ('flu' finds 'influenza'). Use quotes for exact phrases (\\\"influenza vaccine\\\" finds only that exact phrase).<br>     **Example:** influenza vaccine   (optional)
    from_record = '0' # str | Zero-based pagination offset (starting record index)  (optional) (default to '0')
    page_size = '10' # str | Maximum number of records to return per page (optional) (default to '10')
    pre_tag = '<em>' # str | HTML tag to prepend to highlighted search terms in results (optional)
    post_tag = '</em>' # str | HTML tag to append to highlighted search terms in results (optional)
    format = json # str | Response format type (optional) (default to json)
    source_fields = 'source_fields_example' # str | Comma-separated list of specific fields to include in the return response.  ### Study Fields - **study_accession** : PID for the study - **actual_enrollment** : Number of subjects enrolled in the study - **age_range** : age range of the participants involved in the study - **analyte_preferred_count** : The total number of distinct preferred analytes associated with a study. An analyte is a biological substance measured in an assay - **assay_method_count** : The total number of distinct assay methods (measurement techniques) associated with a study. - **assessment_panel_count** : Assesment Panel is collection of assessments which are evaluations ( CRS, questionaires, ratings based on a reference scale) of subjects that do not involve drawing a sample from a subject. The number of the Assessment Panel's in this study - **brief_title** : Short title for the study or trial - **condition_or_disease** : The condition(s)/disease(s) that is (are) being researched or evaluated in the study. - **contract_grant_external_id** : ID from funding source - **contract_grant_name** : Name of the Contract or grant that funded the research. - **doi** : Digital object identifier (DOI) is a type of persistent identifier used to uniquely identify objects. DOI used for the study. - **sex_included** : Indicates the biological sex categories represented among study subjects. - **initial_data_release_date** : Initial date study shared - **initial_data_release_version_number** : Initial version of study shared - **lab_test_panel_count** : Lab Test Panel is a collection of Lab Tests. The number of the Lab Test Panel's in this study - **latest_data_release_version_number** : Latest version of study shared - **latest_data_release_date** : Latest date when the study was shared - **min_age** : The subject age at the outset of the study may be determined form one of several study milestones as indicated in the Age Event column. - **max_age** : The subject age at the end of the study may be determined form one of several study milestones. - **planned_visit_total_count** : Planned Visit describes a STUDY indicated encounter with a SUBJECT. Total number of planned visit in this study - **program_name** : Programs are the NIH organizational basis for administering grants and contracts. - **pubmed_id** : The Pubmed or PubMedCentral identifier of an article that includes data from this study. - **research_focus** : Describes a study's focus, purpose or category. - **shared_subject_count** : The number od participants in the study that have been shared. - **species** : Represents the organism associated with the study or subjects - **study_pi** : The name of the Principal Investigator (PI) responsible for the study.  ### Subject Fields - **study_accession** : PID for the study - **subject_accession** : PID for the subject participant - **arm_name** : The name of the study's arm(s) or cohort(s) group subjects by criteria relevant to the study (e.g. age, condition) and/or treatments or interventions. - **assay_method** : The experimental or laboratory technique used to measure, detect, or quantify biological molecules, cells, or other analytes in a study. - **biosample_type** : The sample types are adopted from Uberon, Cell and CHEBI ontologies. - **clinical_trial** : Indicates if the study is a clinical trial study - **condition_or_disease** : Reported medical conditions or diseases investigated in the study - **ethnicity** : Particpant ethnicity - **sex** : Particpant sex - **has_assessment** : Indicates if the study includes assessment data. Assessment data are evaluations ( CRS, questionaires, ratings based on a reference scale) of subjects that do not involve drawing a sample from a subject. - **has_lab_test** : Indicates if the study includes laboratory test results. Lab Test are laboratory process operating on a biological sample that produces a single value. Similar to an EXPERIMENT, but with a clinical assay focus. - **min_age** : The subject age at the outset of the study may be determined form one of several study milestones as indicated in the Age Event column. - **race** : Particpant race - **research_focus** : Describes a study's focus, purpose or category. - **species** : Represents the organism associated with the study or subjects  **Example:** study_accession,condition_or_disease,brief_title  (optional)
    sort_field = 'sort_field_example' # str | Field name used to sort results.  ### Study Sort Fields - study_accession - actual_enrollment - brief_-  ** - condition_or_disease - contract_grant_name - contract_grant_external_id - doi - sex_included - latest_data_release_version_number - latest_data_release_date - min_age - program_name - pubmed_id - research_focus - species - study_pi  ### Subject Sort Fields - study_accession - subject_accession - arm_name - assay_method - biosample_type - clinical_trial - condition_or_disease - ethnicity - sex - has_assessment - has_lab_test - min_age - race - research_focus - species  **Example:** study_accession  (optional)
    sort_field_direction = asc # str | Sort order direction (optional) (default to asc)
    search_fields = 'search_fields_example' # str | List of specific fields to search within (limits search scope to specified fields). Accepts multiple values comma separated. (optional)
    study_accession = 'study_accession_example' # str | Filter by specific study accession identifier(s). This is the persistant identifier for the study. Accepts multiple values comma separated.  **Example:**   SDY1,SDY2  (optional)
    subject_accession = 'subject_accession_example' # str | Filter by specific subject accession identifier(s). This is the persistant identifier for the subject. Accepts multiple values comma separated. **Example:** SUB00240,SUB00254  (optional)
    program_name = 'program_name_example' # str | Filter by program name(s). Programs are the NIH organizational basis for administering grants and contracts. Accepts multiple values comma separated.   **Example:**   SeroNet,Asthma and Allergic Diseases Cooperative Research Centers (AADCRC) RFA-AI-12-006  (optional)
    condition_or_disease = 'asthma,COVID-19' # str | Filters results to studies/subjects associated with one or more reported medical conditions or diseases investigated in the study. Accepts multiple values comma separated.  Lookup values can be retrieved from: [Disease Lookup API](https://www.immport.org/data/query/api/lookup/lkDisease?format=json)  (optional)
    research_focus = 'research_focus_example' # str |   Filter by research focus area(s). Describes a study's focus, purpose or category. Accepts multiple values comma separated.    Lookup values can be retrieved from:   [Research Focus Lookup API](https://www.immport.org/data/query/api/lookup/lkResearchFocus?format=json)    **Example:** Transplantation,Vaccine Response  (optional)
    clinical_trial = 'clinical_trial_example' # str | Filter to include only clinical trials : Y or N. Accepts multiple values comma separated. (optional)
    sex = 'sex_example' # str |   Filter by participant biological sex(s). Accepts multiple values comma separated.    Lookup values can be retrieved from:   [Sex Lookup API](https://www.immport.org/data/query/api/lookup/lkSex?format=json)    **Example:** Female   (optional)
    race = 'race_example' # str |   Filter by subject race. Accepts multiple values comma separated. Controlled vocabulary for Race follows the census designation and OMB Directive 15.    Lookup values can be retrieved from:   [Race Lookup API](https://www.immport.org/data/query/api/lookup/lkRace?format=json)    **Example:** Asian, White   (optional)
    ethnicity = 'ethnicity_example' # str | Filter by subject ethnicity. Accepts multiple values comma separated. Controlled vocabulary for Ethnicity follows the census designation and OMB Directive 15.  Lookup values can be retrieved from: [Ethnicity Lookup API](https://www.immport.org/data/query/api/lookup/lkSampleType?format=json)   **Example:**  Hispanic or Latino  (optional)
    species = 'species_example' # str | Filter by species studied. Accepts multiple values comma separated. Represents the organism associated with the study or subjects          (e.g., Homo sapiens, Mus musculus).  Lookup values can be retrieved from: [Species Lookup API](https://www.immport.org/data/query/api/lookup/lkSpecies?format=json)   **Example:**     Homo sapiens, Mus musculus  (optional)
    min_age = 'min_age_example' # str | Minimum age of study participants (optional)
    age_range = 'age_range_example' # str | Age range of study participants (e.g., '18-65') (optional)
    assay_method = 'assay_method_example' # str | Filter by assay method(s) used in the study. Accepts multiple values comma separated.  Represents the experimental measurement techniques applied to generate study data (e.g., Flow Cytometry, ELISA, ELISPOT).  Lookup values can be retrieved from: [Assay Method Lookup API](https://www.immport.org/data/query/api/lookup/lkExpMeasurementTech?format=json)   **Example:**     Flow Cytometry, ELISA, ELISPOT  (optional)
    biosample_type = 'biosample_type_example' # str | Filter by biological sample type(s) collected. Accepts multiple values comma separated.  Represents the type of biospecimen obtained from subjects for analysis  Lookup values can be retrieved from: [Biological Sample Type Lookup API](https://www.immport.org/data/query/api/lookup/lkSampleType?format=json)  **Example:** Bone, Cord blood  (optional)
    has_assessment = 'has_assessment_example' # str | Facet filter indicating whether the study includes assessment data.  Evaluations ( CRS, questionaires, ratings based on a reference scale) of subjects that do not involve drawing a sample from a subject.  Accepts one or more of the following values: Y = Includes assessment data N = Does not include assessment data  Multiple values match any of the provided options.  (optional)
    has_lab_test = 'has_lab_test_example' # str | Facet filter indicating whether the study includes laboratory test results.  Laboratory process operating on a biological sample that produces a single value. Similar to an EXPERIMENT, but with a clinical assay focus.  Accepts one or more of the following values: Y = Includes laboratory test results N = Does not include laboratory test results  Multiple values match any of the provided options.  (optional)

    try:
        # Search subjects
        api_response = api_instance.subject_search(term=term, from_record=from_record, page_size=page_size, pre_tag=pre_tag, post_tag=post_tag, format=format, source_fields=source_fields, sort_field=sort_field, sort_field_direction=sort_field_direction, search_fields=search_fields, study_accession=study_accession, subject_accession=subject_accession, program_name=program_name, condition_or_disease=condition_or_disease, research_focus=research_focus, clinical_trial=clinical_trial, sex=sex, race=race, ethnicity=ethnicity, species=species, min_age=min_age, age_range=age_range, assay_method=assay_method, biosample_type=biosample_type, has_assessment=has_assessment, has_lab_test=has_lab_test)
        print("The response of StudySearchApi->subject_search:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudySearchApi->subject_search: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **term** | **str**|     Full-text search term supporting partial matching. Searches within words by default (&#39;flu&#39; finds &#39;influenza&#39;). Use quotes for exact phrases (\\\&quot;influenza vaccine\\\&quot; finds only that exact phrase).&lt;br&gt;     **Example:** influenza vaccine   | [optional] 
 **from_record** | **str**| Zero-based pagination offset (starting record index)  | [optional] [default to &#39;0&#39;]
 **page_size** | **str**| Maximum number of records to return per page | [optional] [default to &#39;10&#39;]
 **pre_tag** | **str**| HTML tag to prepend to highlighted search terms in results | [optional] 
 **post_tag** | **str**| HTML tag to append to highlighted search terms in results | [optional] 
 **format** | **str**| Response format type | [optional] [default to json]
 **source_fields** | **str**| Comma-separated list of specific fields to include in the return response.  ### Study Fields - **study_accession** : PID for the study - **actual_enrollment** : Number of subjects enrolled in the study - **age_range** : age range of the participants involved in the study - **analyte_preferred_count** : The total number of distinct preferred analytes associated with a study. An analyte is a biological substance measured in an assay - **assay_method_count** : The total number of distinct assay methods (measurement techniques) associated with a study. - **assessment_panel_count** : Assesment Panel is collection of assessments which are evaluations ( CRS, questionaires, ratings based on a reference scale) of subjects that do not involve drawing a sample from a subject. The number of the Assessment Panel&#39;s in this study - **brief_title** : Short title for the study or trial - **condition_or_disease** : The condition(s)/disease(s) that is (are) being researched or evaluated in the study. - **contract_grant_external_id** : ID from funding source - **contract_grant_name** : Name of the Contract or grant that funded the research. - **doi** : Digital object identifier (DOI) is a type of persistent identifier used to uniquely identify objects. DOI used for the study. - **sex_included** : Indicates the biological sex categories represented among study subjects. - **initial_data_release_date** : Initial date study shared - **initial_data_release_version_number** : Initial version of study shared - **lab_test_panel_count** : Lab Test Panel is a collection of Lab Tests. The number of the Lab Test Panel&#39;s in this study - **latest_data_release_version_number** : Latest version of study shared - **latest_data_release_date** : Latest date when the study was shared - **min_age** : The subject age at the outset of the study may be determined form one of several study milestones as indicated in the Age Event column. - **max_age** : The subject age at the end of the study may be determined form one of several study milestones. - **planned_visit_total_count** : Planned Visit describes a STUDY indicated encounter with a SUBJECT. Total number of planned visit in this study - **program_name** : Programs are the NIH organizational basis for administering grants and contracts. - **pubmed_id** : The Pubmed or PubMedCentral identifier of an article that includes data from this study. - **research_focus** : Describes a study&#39;s focus, purpose or category. - **shared_subject_count** : The number od participants in the study that have been shared. - **species** : Represents the organism associated with the study or subjects - **study_pi** : The name of the Principal Investigator (PI) responsible for the study.  ### Subject Fields - **study_accession** : PID for the study - **subject_accession** : PID for the subject participant - **arm_name** : The name of the study&#39;s arm(s) or cohort(s) group subjects by criteria relevant to the study (e.g. age, condition) and/or treatments or interventions. - **assay_method** : The experimental or laboratory technique used to measure, detect, or quantify biological molecules, cells, or other analytes in a study. - **biosample_type** : The sample types are adopted from Uberon, Cell and CHEBI ontologies. - **clinical_trial** : Indicates if the study is a clinical trial study - **condition_or_disease** : Reported medical conditions or diseases investigated in the study - **ethnicity** : Particpant ethnicity - **sex** : Particpant sex - **has_assessment** : Indicates if the study includes assessment data. Assessment data are evaluations ( CRS, questionaires, ratings based on a reference scale) of subjects that do not involve drawing a sample from a subject. - **has_lab_test** : Indicates if the study includes laboratory test results. Lab Test are laboratory process operating on a biological sample that produces a single value. Similar to an EXPERIMENT, but with a clinical assay focus. - **min_age** : The subject age at the outset of the study may be determined form one of several study milestones as indicated in the Age Event column. - **race** : Particpant race - **research_focus** : Describes a study&#39;s focus, purpose or category. - **species** : Represents the organism associated with the study or subjects  **Example:** study_accession,condition_or_disease,brief_title  | [optional] 
 **sort_field** | **str**| Field name used to sort results.  ### Study Sort Fields - study_accession - actual_enrollment - brief_-  ** - condition_or_disease - contract_grant_name - contract_grant_external_id - doi - sex_included - latest_data_release_version_number - latest_data_release_date - min_age - program_name - pubmed_id - research_focus - species - study_pi  ### Subject Sort Fields - study_accession - subject_accession - arm_name - assay_method - biosample_type - clinical_trial - condition_or_disease - ethnicity - sex - has_assessment - has_lab_test - min_age - race - research_focus - species  **Example:** study_accession  | [optional] 
 **sort_field_direction** | **str**| Sort order direction | [optional] [default to asc]
 **search_fields** | **str**| List of specific fields to search within (limits search scope to specified fields). Accepts multiple values comma separated. | [optional] 
 **study_accession** | **str**| Filter by specific study accession identifier(s). This is the persistant identifier for the study. Accepts multiple values comma separated.  **Example:**   SDY1,SDY2  | [optional] 
 **subject_accession** | **str**| Filter by specific subject accession identifier(s). This is the persistant identifier for the subject. Accepts multiple values comma separated. **Example:** SUB00240,SUB00254  | [optional] 
 **program_name** | **str**| Filter by program name(s). Programs are the NIH organizational basis for administering grants and contracts. Accepts multiple values comma separated.   **Example:**   SeroNet,Asthma and Allergic Diseases Cooperative Research Centers (AADCRC) RFA-AI-12-006  | [optional] 
 **condition_or_disease** | **str**| Filters results to studies/subjects associated with one or more reported medical conditions or diseases investigated in the study. Accepts multiple values comma separated.  Lookup values can be retrieved from: [Disease Lookup API](https://www.immport.org/data/query/api/lookup/lkDisease?format&#x3D;json)  | [optional] 
 **research_focus** | **str**|   Filter by research focus area(s). Describes a study&#39;s focus, purpose or category. Accepts multiple values comma separated.    Lookup values can be retrieved from:   [Research Focus Lookup API](https://www.immport.org/data/query/api/lookup/lkResearchFocus?format&#x3D;json)    **Example:** Transplantation,Vaccine Response  | [optional] 
 **clinical_trial** | **str**| Filter to include only clinical trials : Y or N. Accepts multiple values comma separated. | [optional] 
 **sex** | **str**|   Filter by participant biological sex(s). Accepts multiple values comma separated.    Lookup values can be retrieved from:   [Sex Lookup API](https://www.immport.org/data/query/api/lookup/lkSex?format&#x3D;json)    **Example:** Female   | [optional] 
 **race** | **str**|   Filter by subject race. Accepts multiple values comma separated. Controlled vocabulary for Race follows the census designation and OMB Directive 15.    Lookup values can be retrieved from:   [Race Lookup API](https://www.immport.org/data/query/api/lookup/lkRace?format&#x3D;json)    **Example:** Asian, White   | [optional] 
 **ethnicity** | **str**| Filter by subject ethnicity. Accepts multiple values comma separated. Controlled vocabulary for Ethnicity follows the census designation and OMB Directive 15.  Lookup values can be retrieved from: [Ethnicity Lookup API](https://www.immport.org/data/query/api/lookup/lkSampleType?format&#x3D;json)   **Example:**  Hispanic or Latino  | [optional] 
 **species** | **str**| Filter by species studied. Accepts multiple values comma separated. Represents the organism associated with the study or subjects          (e.g., Homo sapiens, Mus musculus).  Lookup values can be retrieved from: [Species Lookup API](https://www.immport.org/data/query/api/lookup/lkSpecies?format&#x3D;json)   **Example:**     Homo sapiens, Mus musculus  | [optional] 
 **min_age** | **str**| Minimum age of study participants | [optional] 
 **age_range** | **str**| Age range of study participants (e.g., &#39;18-65&#39;) | [optional] 
 **assay_method** | **str**| Filter by assay method(s) used in the study. Accepts multiple values comma separated.  Represents the experimental measurement techniques applied to generate study data (e.g., Flow Cytometry, ELISA, ELISPOT).  Lookup values can be retrieved from: [Assay Method Lookup API](https://www.immport.org/data/query/api/lookup/lkExpMeasurementTech?format&#x3D;json)   **Example:**     Flow Cytometry, ELISA, ELISPOT  | [optional] 
 **biosample_type** | **str**| Filter by biological sample type(s) collected. Accepts multiple values comma separated.  Represents the type of biospecimen obtained from subjects for analysis  Lookup values can be retrieved from: [Biological Sample Type Lookup API](https://www.immport.org/data/query/api/lookup/lkSampleType?format&#x3D;json)  **Example:** Bone, Cord blood  | [optional] 
 **has_assessment** | **str**| Facet filter indicating whether the study includes assessment data.  Evaluations ( CRS, questionaires, ratings based on a reference scale) of subjects that do not involve drawing a sample from a subject.  Accepts one or more of the following values: Y &#x3D; Includes assessment data N &#x3D; Does not include assessment data  Multiple values match any of the provided options.  | [optional] 
 **has_lab_test** | **str**| Facet filter indicating whether the study includes laboratory test results.  Laboratory process operating on a biological sample that produces a single value. Similar to an EXPERIMENT, but with a clinical assay focus.  Accepts one or more of the following values: Y &#x3D; Includes laboratory test results N &#x3D; Does not include laboratory test results  Multiple values match any of the provided options.  | [optional] 

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Search results returned successfully. |  -  |
**401** | Unauthorized (missing/invalid token). |  -  |
**400** | Invalid query parameters. |  -  |
**403** | Forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

