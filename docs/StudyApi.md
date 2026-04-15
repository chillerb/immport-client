# StudyApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**study_accession** | **str** |  | [optional] 
**actual_completion_date** | **str** |  | [optional] 
**actual_enrollment** | **int** |  | [optional] 
**actual_start_date** | **str** |  | [optional] 
**age_unit** | **str** |  | [optional] 
**brief_description** | **str** |  | [optional] 
**brief_title** | **str** |  | [optional] 
**clinical_trial** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**dcl_id** | **int** |  | [optional] 
**doi** | **str** |  | [optional] 
**endpoints** | **str** |  | [optional] 
**gender_included** | **str** |  | [optional] 
**hypothesis** | **str** |  | [optional] 
**initial_data_release_date** | **str** |  | [optional] 
**initial_data_release_version** | **str** |  | [optional] 
**intervention_agent** | **str** |  | [optional] 
**latest_data_release_date** | **str** |  | [optional] 
**latest_data_release_version** | **str** |  | [optional] 
**maximum_age** | **str** |  | [optional] 
**minimum_age** | **str** |  | [optional] 
**objectives** | **str** |  | [optional] 
**official_title** | **str** |  | [optional] 
**shared_study** | **str** |  | [optional] 
**sponsoring_organization** | **str** |  | [optional] 
**target_enrollment** | **int** |  | [optional] 

## Example

```python
from immport_client.models.study_api import StudyApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyApi from a JSON string
study_api_instance = StudyApi.from_json(json)
# print the JSON string representation of the object
print(StudyApi.to_json())

# convert the object into a dict
study_api_dict = study_api_instance.to_dict()
# create an instance of StudyApi from a dict
study_api_from_dict = StudyApi.from_dict(study_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


