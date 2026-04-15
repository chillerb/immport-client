# StudyLinkApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**study_link_id** | **int** |  | [optional] 
**study_accession** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**value** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_link_api import StudyLinkApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyLinkApi from a JSON string
study_link_api_instance = StudyLinkApi.from_json(json)
# print the JSON string representation of the object
print(StudyLinkApi.to_json())

# convert the object into a dict
study_link_api_dict = study_link_api_instance.to_dict()
# create an instance of StudyLinkApi from a dict
study_link_api_from_dict = StudyLinkApi.from_dict(study_link_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


