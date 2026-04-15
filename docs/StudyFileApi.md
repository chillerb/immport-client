# StudyFileApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**study_file_accession** | **str** |  | [optional] 
**study_accession** | **str** |  | [optional] 
**study_file_type** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**file_name** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_file_api import StudyFileApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyFileApi from a JSON string
study_file_api_instance = StudyFileApi.from_json(json)
# print the JSON string representation of the object
print(StudyFileApi.to_json())

# convert the object into a dict
study_file_api_dict = study_file_api_instance.to_dict()
# create an instance of StudyFileApi from a dict
study_file_api_from_dict = StudyFileApi.from_dict(study_file_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


