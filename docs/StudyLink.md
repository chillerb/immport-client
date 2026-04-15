# StudyLink


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**study_link_id** | **int** |  | [optional] 
**name** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**value** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_link import StudyLink

# TODO update the JSON string below
json = "{}"
# create an instance of StudyLink from a JSON string
study_link_instance = StudyLink.from_json(json)
# print the JSON string representation of the object
print(StudyLink.to_json())

# convert the object into a dict
study_link_dict = study_link_instance.to_dict()
# create an instance of StudyLink from a dict
study_link_from_dict = StudyLink.from_dict(study_link_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


