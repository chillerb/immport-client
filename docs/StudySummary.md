# StudySummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**study_accession** | **str** |  | [optional] 
**doi** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**pi** | **str** |  | [optional] 
**condition_studied** | **str** |  | [optional] 
**research_focus** | **str** |  | [optional] 
**brief_description** | **str** |  | [optional] 
**start_date** | **str** |  | [optional] 
**detailed_description** | **str** |  | [optional] 
**objectives** | **str** |  | [optional] 
**endpoints** | **str** |  | [optional] 
**gender_included** | **str** |  | [optional] 
**sex_included** | **str** |  | [optional] 
**subjects_number** | **int** |  | [optional] 
**download_packages** | **str** |  | [optional] 
**contract_grant** | **str** |  | [optional] 
**program** | **str** |  | [optional] 
**data_completeness** | **str** |  | [optional] 
**hypothesis** | **str** |  | [optional] 
**shared_study** | **str** |  | [optional] 
**intervention_agent** | **str** |  | [optional] 
**initial_data_release_date** | **str** |  | [optional] 
**initial_data_release_version** | **str** |  | [optional] 
**latest_data_release_date** | **str** |  | [optional] 
**latest_data_release_version** | **str** |  | [optional] 
**study_links** | [**List[StudyLink]**](StudyLink.md) |  | [optional] 
**study_pubmeds** | [**List[StudyPubmed]**](StudyPubmed.md) |  | [optional] 
**study_personnel** | [**List[StudyPersonnel]**](StudyPersonnel.md) |  | [optional] 

## Example

```python
from immport_client.models.study_summary import StudySummary

# TODO update the JSON string below
json = "{}"
# create an instance of StudySummary from a JSON string
study_summary_instance = StudySummary.from_json(json)
# print the JSON string representation of the object
print(StudySummary.to_json())

# convert the object into a dict
study_summary_dict = study_summary_instance.to_dict()
# create an instance of StudySummary from a dict
study_summary_from_dict = StudySummary.from_dict(study_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


