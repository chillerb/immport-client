# StudySubjectBioSampleApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**study_accession** | **str** |  | [optional] 
**brief_title** | **str** |  | [optional] 
**arm_accession** | **str** |  | [optional] 
**arm_name** | **str** |  | [optional] 
**arm_description** | **str** |  | [optional] 
**arm_type_reported** | **str** |  | [optional] 
**arm_type_preferred** | **str** |  | [optional] 
**subject_accession** | **str** |  | [optional] 
**age_event** | **str** |  | [optional] 
**age_event_specify** | **str** |  | [optional] 
**age_unit** | **str** |  | [optional] 
**max_subject_age** | **float** |  | [optional] 
**min_subject_age** | **float** |  | [optional] 
**subject_phenotype** | **str** |  | [optional] 
**subject_location** | **str** |  | [optional] 
**max_subject_age_in_years** | **str** |  | [optional] 
**min_subject_age_in_years** | **str** |  | [optional] 
**ancestral_population** | **str** |  | [optional] 
**subject_description** | **str** |  | [optional] 
**ethnicity** | **str** |  | [optional] 
**gender** | **str** |  | [optional] 
**race** | **str** |  | [optional] 
**race_specify** | **str** |  | [optional] 
**species** | **str** |  | [optional] 
**strain** | **str** |  | [optional] 
**strain_characteristics** | **str** |  | [optional] 
**biosample_accession** | **str** |  | [optional] 
**planned_visit_accession** | **str** |  | [optional] 
**biosample_name** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**subtype** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_subject_bio_sample_api import StudySubjectBioSampleApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudySubjectBioSampleApi from a JSON string
study_subject_bio_sample_api_instance = StudySubjectBioSampleApi.from_json(json)
# print the JSON string representation of the object
print(StudySubjectBioSampleApi.to_json())

# convert the object into a dict
study_subject_bio_sample_api_dict = study_subject_bio_sample_api_instance.to_dict()
# create an instance of StudySubjectBioSampleApi from a dict
study_subject_bio_sample_api_from_dict = StudySubjectBioSampleApi.from_dict(study_subject_bio_sample_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


