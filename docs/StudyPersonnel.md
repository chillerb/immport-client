# StudyPersonnel


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**person_accession** | **str** |  | [optional] 
**role_in_study** | **str** |  | [optional] 
**site_name** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**first_name** | **str** |  | [optional] 
**honorific** | **str** |  | [optional] 
**last_name** | **str** |  | [optional] 
**organization** | **str** |  | [optional] 
**suffixes** | **str** |  | [optional] 
**title_in_study** | **str** |  | [optional] 
**workspace_id** | **int** |  | [optional] 

## Example

```python
from immport_client.models.study_personnel import StudyPersonnel

# TODO update the JSON string below
json = "{}"
# create an instance of StudyPersonnel from a JSON string
study_personnel_instance = StudyPersonnel.from_json(json)
# print the JSON string representation of the object
print(StudyPersonnel.to_json())

# convert the object into a dict
study_personnel_dict = study_personnel_instance.to_dict()
# create an instance of StudyPersonnel from a dict
study_personnel_from_dict = StudyPersonnel.from_dict(study_personnel_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


