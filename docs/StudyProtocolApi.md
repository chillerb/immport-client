# StudyProtocolApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**study_accession** | **str** |  | [optional] 
**protocol_accession** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**file_name** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**original_file_name** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_protocol_api import StudyProtocolApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyProtocolApi from a JSON string
study_protocol_api_instance = StudyProtocolApi.from_json(json)
# print the JSON string representation of the object
print(StudyProtocolApi.to_json())

# convert the object into a dict
study_protocol_api_dict = study_protocol_api_instance.to_dict()
# create an instance of StudyProtocolApi from a dict
study_protocol_api_from_dict = StudyProtocolApi.from_dict(study_protocol_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


