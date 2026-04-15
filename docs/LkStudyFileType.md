# LkStudyFileType


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_study_file_type import LkStudyFileType

# TODO update the JSON string below
json = "{}"
# create an instance of LkStudyFileType from a JSON string
lk_study_file_type_instance = LkStudyFileType.from_json(json)
# print the JSON string representation of the object
print(LkStudyFileType.to_json())

# convert the object into a dict
lk_study_file_type_dict = lk_study_file_type_instance.to_dict()
# create an instance of LkStudyFileType from a dict
lk_study_file_type_from_dict = LkStudyFileType.from_dict(lk_study_file_type_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


