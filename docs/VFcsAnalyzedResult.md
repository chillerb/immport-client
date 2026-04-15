# VFcsAnalyzedResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result_id** | **int** |  | [optional] 
**age_event** | **str** |  | [optional] 
**age_event_specify** | **str** |  | [optional] 
**age_unit** | **str** |  | [optional] 
**ancestral_population** | **str** |  | [optional] 
**arm_accession** | **str** |  | [optional] 
**arm_name** | **str** |  | [optional] 
**biosample_accession** | **str** |  | [optional] 
**biosample_type** | **str** |  | [optional] 
**biosample_subtype** | **str** |  | [optional] 
**clinical** | **str** |  | [optional] 
**comments** | **str** |  | [optional] 
**ethnicity** | **str** |  | [optional] 
**experiment_accession** | **str** |  | [optional] 
**expsample_accession** | **str** |  | [optional] 
**gender** | **str** |  | [optional] 
**max_subject_age** | **float** |  | [optional] 
**measurement_technique** | **str** |  | [optional] 
**min_subject_age** | **float** |  | [optional] 
**parent_population_preferred** | **str** |  | [optional] 
**parent_population_reported** | **str** |  | [optional] 
**population_defnition_preferred** | **str** |  | [optional] 
**population_defnition_reported** | **str** |  | [optional] 
**population_name_preferred** | **str** |  | [optional] 
**population_name_reported** | **str** |  | [optional] 
**population_stat_unit_preferred** | **str** |  | [optional] 
**population_stat_unit_reported** | **str** |  | [optional] 
**population_statistic_preferred** | **float** |  | [optional] 
**population_statistic_reported** | **str** |  | [optional] 
**planned_visit_accession** | **str** |  | [optional] 
**race** | **str** |  | [optional] 
**race_specify** | **str** |  | [optional] 
**repository_accession** | **str** |  | [optional] 
**repository_name** | **str** |  | [optional] 
**species** | **str** |  | [optional] 
**strain** | **str** |  | [optional] 
**study_accession** | **str** |  | [optional] 
**study_title** | **str** |  | [optional] 
**study_time_collected** | **float** |  | [optional] 
**study_time_collected_unit** | **str** |  | [optional] 
**study_time_t0_event** | **str** |  | [optional] 
**study_time_t0_event_specify** | **str** |  | [optional] 
**subject_accession** | **str** |  | [optional] 
**subject_phenotype** | **str** |  | [optional] 
**workspace_file_info_id** | **int** |  | [optional] 
**treatment_accession** | **str** |  | [optional] 

## Example

```python
from immport_client.models.v_fcs_analyzed_result import VFcsAnalyzedResult

# TODO update the JSON string below
json = "{}"
# create an instance of VFcsAnalyzedResult from a JSON string
v_fcs_analyzed_result_instance = VFcsAnalyzedResult.from_json(json)
# print the JSON string representation of the object
print(VFcsAnalyzedResult.to_json())

# convert the object into a dict
v_fcs_analyzed_result_dict = v_fcs_analyzed_result_instance.to_dict()
# create an instance of VFcsAnalyzedResult from a dict
v_fcs_analyzed_result_from_dict = VFcsAnalyzedResult.from_dict(v_fcs_analyzed_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


