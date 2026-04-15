# FileDetails


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_details_id** | **float** |  | [optional] 
**reported_md5** | **str** |  | [optional] 
**generated_md5** | **str** |  | [optional] 
**study_accession** | **str** |  | [optional] 
**filesize_bytes** | **int** |  | [optional] 
**file_type** | **str** |  | [optional] 
**file_accession** | **str** |  | [optional] 
**file_name** | **str** |  | [optional] 
**path** | **str** |  | [optional] 
**date_file_updated** | **datetime** |  | [optional] 
**file_uuid** | **str** |  | [optional] 
**drs_object_created** | **str** |  | [optional] 
**workspace_id** | **int** |  | [optional] 
**aigenerated_keywords** | **str** |  | [optional] 
**aigenerated_summary** | **str** |  | [optional] 

## Example

```python
from immport_client.models.file_details import FileDetails

# TODO update the JSON string below
json = "{}"
# create an instance of FileDetails from a JSON string
file_details_instance = FileDetails.from_json(json)
# print the JSON string representation of the object
print(FileDetails.to_json())

# convert the object into a dict
file_details_dict = file_details_instance.to_dict()
# create an instance of FileDetails from a dict
file_details_from_dict = FileDetails.from_dict(file_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


