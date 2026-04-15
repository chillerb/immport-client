# VPcrResult


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
**gene_id** | **str** |  | [optional] 
**gene_name** | **str** |  | [optional] 
**analyte_accession** | **str** |  | [optional] 
**gene_symbol_reported** | **str** |  | [optional] 
**gene_symbol_preferred** | **str** |  | [optional] 
**max_subject_age** | **float** |  | [optional] 
**measurement_technique** | **str** |  | [optional] 
**min_subject_age** | **float** |  | [optional] 
**other_gene_accession** | **str** |  | [optional] 
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
**unit_preferred** | **str** |  | [optional] 
**unit_reported** | **str** |  | [optional] 
**value_preferred** | **float** |  | [optional] 
**value_reported** | **str** |  | [optional] 
**treatment_accession** | **str** |  | [optional] 

## Example

```python
from immport_client.models.v_pcr_result import VPcrResult

# TODO update the JSON string below
json = "{}"
# create an instance of VPcrResult from a JSON string
v_pcr_result_instance = VPcrResult.from_json(json)
# print the JSON string representation of the object
print(VPcrResult.to_json())

# convert the object into a dict
v_pcr_result_dict = v_pcr_result_instance.to_dict()
# create an instance of VPcrResult from a dict
v_pcr_result_from_dict = VPcrResult.from_dict(v_pcr_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


