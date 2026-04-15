# StudyExperimentApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**experiment_accession** | **str** |  | [optional] 
**study_accession** | **str** |  | [optional] 
**measurement_technique** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**name** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_experiment_api import StudyExperimentApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyExperimentApi from a JSON string
study_experiment_api_instance = StudyExperimentApi.from_json(json)
# print the JSON string representation of the object
print(StudyExperimentApi.to_json())

# convert the object into a dict
study_experiment_api_dict = study_experiment_api_instance.to_dict()
# create an instance of StudyExperimentApi from a dict
study_experiment_api_from_dict = StudyExperimentApi.from_dict(study_experiment_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


