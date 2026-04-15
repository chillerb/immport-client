# StudyConditionOrDiseaseApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**study_accession** | **str** |  | [optional] 
**condition_reported** | **str** |  | [optional] 
**condition_preferred** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_condition_or_disease_api import StudyConditionOrDiseaseApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyConditionOrDiseaseApi from a JSON string
study_condition_or_disease_api_instance = StudyConditionOrDiseaseApi.from_json(json)
# print the JSON string representation of the object
print(StudyConditionOrDiseaseApi.to_json())

# convert the object into a dict
study_condition_or_disease_api_dict = study_condition_or_disease_api_instance.to_dict()
# create an instance of StudyConditionOrDiseaseApi from a dict
study_condition_or_disease_api_from_dict = StudyConditionOrDiseaseApi.from_dict(study_condition_or_disease_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


