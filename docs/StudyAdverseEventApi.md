# StudyAdverseEventApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**adverse_event_accession** | **str** |  | [optional] 
**study_accession** | **str** |  | [optional] 
**subject_accession** | **str** |  | [optional] 
**causality** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**end_study_day** | **float** |  | [optional] 
**end_time** | **str** |  | [optional] 
**location_of_reaction_preferred** | **str** |  | [optional] 
**location_of_reaction_reported** | **str** |  | [optional] 
**name_preferred** | **str** |  | [optional] 
**name_reported** | **str** |  | [optional] 
**organ_or_body_system_preferred** | **str** |  | [optional] 
**organ_or_body_system_reported** | **str** |  | [optional] 
**other_action_taken** | **str** |  | [optional] 
**outcome_preferred** | **str** |  | [optional] 
**outcome_reported** | **str** |  | [optional] 
**relation_to_nonstudy_treatment** | **str** |  | [optional] 
**relation_to_study_treatment** | **str** |  | [optional] 
**severity_reported** | **str** |  | [optional] 
**severity_preferred** | **str** |  | [optional] 
**start_study_day** | **float** |  | [optional] 
**start_time** | **str** |  | [optional] 
**study_treatment_action_taken** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_adverse_event_api import StudyAdverseEventApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyAdverseEventApi from a JSON string
study_adverse_event_api_instance = StudyAdverseEventApi.from_json(json)
# print the JSON string representation of the object
print(StudyAdverseEventApi.to_json())

# convert the object into a dict
study_adverse_event_api_dict = study_adverse_event_api_instance.to_dict()
# create an instance of StudyAdverseEventApi from a dict
study_adverse_event_api_from_dict = StudyAdverseEventApi.from_dict(study_adverse_event_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


