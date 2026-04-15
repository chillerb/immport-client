# StudySubjectInterventionApi


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
**intervention_accession** | **str** |  | [optional] 
**compound_name_reported** | **str** |  | [optional] 
**compound_role** | **str** |  | [optional] 
**dose** | **str** |  | [optional] 
**dose_freq_per_interval** | **str** |  | [optional] 
**dose_reported** | **str** |  | [optional] 
**dose_units** | **str** |  | [optional] 
**duration** | **str** |  | [optional] 
**duration_unit** | **str** |  | [optional] 
**end_day** | **str** |  | [optional] 
**end_time** | **str** |  | [optional] 
**formulation** | **str** |  | [optional] 
**is_ongoing** | **str** |  | [optional] 
**name_preferred** | **str** |  | [optional] 
**name_reported** | **str** |  | [optional] 
**reported_indication** | **str** |  | [optional] 
**route_of_admin_preferred** | **str** |  | [optional] 
**route_of_admin_reported** | **str** |  | [optional] 
**start_day** | **str** |  | [optional] 
**start_time** | **str** |  | [optional] 
**status** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_subject_intervention_api import StudySubjectInterventionApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudySubjectInterventionApi from a JSON string
study_subject_intervention_api_instance = StudySubjectInterventionApi.from_json(json)
# print the JSON string representation of the object
print(StudySubjectInterventionApi.to_json())

# convert the object into a dict
study_subject_intervention_api_dict = study_subject_intervention_api_instance.to_dict()
# create an instance of StudySubjectInterventionApi from a dict
study_subject_intervention_api_from_dict = StudySubjectInterventionApi.from_dict(study_subject_intervention_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


