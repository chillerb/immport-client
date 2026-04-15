# StudyFileDetailsApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_details_id** | **float** |  | [optional] 
**generated_md5** | **str** |  | [optional] 
**study_accession** | **str** |  | [optional] 
**file_type** | **str** |  | [optional] 
**file_accession** | **str** |  | [optional] 
**file_name** | **str** |  | [optional] 
**path** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_file_details_api import StudyFileDetailsApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyFileDetailsApi from a JSON string
study_file_details_api_instance = StudyFileDetailsApi.from_json(json)
# print the JSON string representation of the object
print(StudyFileDetailsApi.to_json())

# convert the object into a dict
study_file_details_api_dict = study_file_details_api_instance.to_dict()
# create an instance of StudyFileDetailsApi from a dict
study_file_details_api_from_dict = StudyFileDetailsApi.from_dict(study_file_details_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


