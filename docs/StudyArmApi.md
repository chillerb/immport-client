# StudyArmApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**arm_accession** | **str** |  | [optional] 
**study_accession** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**type_reported** | **str** |  | [optional] 
**type_preferred** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_arm_api import StudyArmApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyArmApi from a JSON string
study_arm_api_instance = StudyArmApi.from_json(json)
# print the JSON string representation of the object
print(StudyArmApi.to_json())

# convert the object into a dict
study_arm_api_dict = study_arm_api_instance.to_dict()
# create an instance of StudyArmApi from a dict
study_arm_api_from_dict = StudyArmApi.from_dict(study_arm_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


