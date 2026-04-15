# ResultFilePath


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_path_id** | **str** |  | [optional] 
**file_info_id** | **int** |  | [optional] 
**file_detail** | **str** |  | [optional] 
**filesize_bytes** | **int** |  | [optional] 
**file_name** | **str** |  | [optional] 
**original_file_name** | **str** |  | [optional] 
**source_type** | **str** |  | [optional] 
**source_accession** | **str** |  | [optional] 
**experiment_accession** | **str** |  | [optional] 
**measurement_technique** | **str** |  | [optional] 
**study_accession** | **str** |  | [optional] 
**clinical** | **str** |  | [optional] 
**study_title** | **str** |  | [optional] 
**biosample_accession** | **str** |  | [optional] 
**biosample_type** | **str** |  | [optional] 
**biosample_subtype** | **str** |  | [optional] 
**study_time_collected** | **float** |  | [optional] 
**study_time_collected_unit** | **str** |  | [optional] 
**study_time_t0_event** | **str** |  | [optional] 
**study_time_t0_event_specify** | **str** |  | [optional] 
**planned_visit_accession** | **str** |  | [optional] 
**subject_accession** | **str** |  | [optional] 
**ethnicity** | **str** |  | [optional] 
**gender** | **str** |  | [optional] 
**race** | **str** |  | [optional] 
**race_specify** | **str** |  | [optional] 
**species** | **str** |  | [optional] 
**strain** | **str** |  | [optional] 
**arm_accession** | **str** |  | [optional] 
**arm_name** | **str** |  | [optional] 
**age_event** | **str** |  | [optional] 
**age_event_specify** | **str** |  | [optional] 
**age_unit** | **str** |  | [optional] 
**max_subject_age** | **float** |  | [optional] 
**min_subject_age** | **float** |  | [optional] 
**subject_phenotype** | **str** |  | [optional] 
**file_path** | **str** |  | [optional] 

## Example

```python
from immport_client.models.result_file_path import ResultFilePath

# TODO update the JSON string below
json = "{}"
# create an instance of ResultFilePath from a JSON string
result_file_path_instance = ResultFilePath.from_json(json)
# print the JSON string representation of the object
print(ResultFilePath.to_json())

# convert the object into a dict
result_file_path_dict = result_file_path_instance.to_dict()
# create an instance of ResultFilePath from a dict
result_file_path_from_dict = ResultFilePath.from_dict(result_file_path_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


