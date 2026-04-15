# VMbaaResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result_id** | **int** |  | [optional] 
**age_event** | **str** |  | [optional] 
**age_event_specify** | **str** |  | [optional] 
**age_unit** | **str** |  | [optional] 
**ancestral_population** | **str** |  | [optional] 
**analyte_accession** | **str** |  | [optional] 
**analyte_preferred** | **str** |  | [optional] 
**analyte_reported** | **str** |  | [optional] 
**arm_accession** | **str** |  | [optional] 
**arm_name** | **str** |  | [optional] 
**assay_group_id** | **str** |  | [optional] 
**assay_id** | **str** |  | [optional] 
**biosample_accession** | **str** |  | [optional] 
**biosample_type** | **str** |  | [optional] 
**biosample_subtype** | **str** |  | [optional] 
**clinical** | **str** |  | [optional] 
**comments** | **str** |  | [optional] 
**concentration_unit_preferred** | **str** |  | [optional] 
**concentration_unit_reported** | **str** |  | [optional] 
**concentration_value_preferred** | **float** |  | [optional] 
**concentration_value_reported** | **str** |  | [optional] 
**ethnicity** | **str** |  | [optional] 
**experiment_accession** | **str** |  | [optional] 
**gender** | **str** |  | [optional] 
**max_subject_age** | **float** |  | [optional] 
**measurement_technique** | **str** |  | [optional] 
**mfi** | **str** |  | [optional] 
**mfi_coordinate** | **str** |  | [optional] 
**min_subject_age** | **float** |  | [optional] 
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
**source_accession** | **str** |  | [optional] 
**source_type** | **str** |  | [optional] 
**subject_accession** | **str** |  | [optional] 
**subject_phenotype** | **str** |  | [optional] 
**treatment_accession** | **str** |  | [optional] 

## Example

```python
from immport_client.models.v_mbaa_result import VMbaaResult

# TODO update the JSON string below
json = "{}"
# create an instance of VMbaaResult from a JSON string
v_mbaa_result_instance = VMbaaResult.from_json(json)
# print the JSON string representation of the object
print(VMbaaResult.to_json())

# convert the object into a dict
v_mbaa_result_dict = v_mbaa_result_instance.to_dict()
# create an instance of VMbaaResult from a dict
v_mbaa_result_from_dict = VMbaaResult.from_dict(v_mbaa_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


