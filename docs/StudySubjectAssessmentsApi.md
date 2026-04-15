# StudySubjectAssessmentsApi


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
**assessment_panel_accession** | **str** |  | [optional] 
**assessment_type** | **str** |  | [optional] 
**assessment_panel_name_preferred** | **str** |  | [optional] 
**assessment_panel_name_reported** | **str** |  | [optional] 
**result_schema** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**assessment_component_accession** | **str** |  | [optional] 
**age_at_onset_preferred** | **str** |  | [optional] 
**age_at_onset_reported** | **str** |  | [optional] 
**age_at_onset_unit_preferred** | **str** |  | [optional] 
**age_at_onset_unit_reported** | **str** |  | [optional] 
**is_clinically_significant** | **str** |  | [optional] 
**location_of_finding_preferred** | **str** |  | [optional] 
**location_of_finding_reported** | **str** |  | [optional] 
**assessment_component_name_preferred** | **str** |  | [optional] 
**assessment_component_name_reported** | **str** |  | [optional] 
**organ_or_body_system_preferred** | **str** |  | [optional] 
**organ_or_body_system_reported** | **str** |  | [optional] 
**planned_visit_accession** | **str** |  | [optional] 
**reference_range_accession** | **str** |  | [optional] 
**result_unit_preferred** | **str** |  | [optional] 
**result_unit_reported** | **str** |  | [optional] 
**result_value_category** | **str** |  | [optional] 
**result_value_preferred** | **str** |  | [optional] 
**result_value_reported** | **str** |  | [optional] 
**study_day** | **str** |  | [optional] 
**subject_position_preferred** | **str** |  | [optional] 
**subject_position_reported** | **str** |  | [optional] 
**time_of_day** | **str** |  | [optional] 
**verbatim_question** | **str** |  | [optional] 
**who_is_assessed** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_subject_assessments_api import StudySubjectAssessmentsApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudySubjectAssessmentsApi from a JSON string
study_subject_assessments_api_instance = StudySubjectAssessmentsApi.from_json(json)
# print the JSON string representation of the object
print(StudySubjectAssessmentsApi.to_json())

# convert the object into a dict
study_subject_assessments_api_dict = study_subject_assessments_api_instance.to_dict()
# create an instance of StudySubjectAssessmentsApi from a dict
study_subject_assessments_api_from_dict = StudySubjectAssessmentsApi.from_dict(study_subject_assessments_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


