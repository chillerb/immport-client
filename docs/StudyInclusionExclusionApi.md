# StudyInclusionExclusionApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**criterion_accession** | **str** |  | [optional] 
**criterion_category** | **str** |  | [optional] 
**criterion** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_inclusion_exclusion_api import StudyInclusionExclusionApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyInclusionExclusionApi from a JSON string
study_inclusion_exclusion_api_instance = StudyInclusionExclusionApi.from_json(json)
# print the JSON string representation of the object
print(StudyInclusionExclusionApi.to_json())

# convert the object into a dict
study_inclusion_exclusion_api_dict = study_inclusion_exclusion_api_instance.to_dict()
# create an instance of StudyInclusionExclusionApi from a dict
study_inclusion_exclusion_api_from_dict = StudyInclusionExclusionApi.from_dict(study_inclusion_exclusion_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


