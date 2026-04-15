# FilterCriteriaFields


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**age_event** | **List[str]** |  | [optional] 
**age_event_specify** | **List[str]** |  | [optional] 
**age_unit** | **List[str]** |  | [optional] 
**ancestral_population** | **List[str]** |  | [optional] 
**arm_accession** | **List[str]** |  | [optional] 
**arm_name** | **List[str]** |  | [optional] 
**biosample_accession** | **List[str]** |  | [optional] 
**biosample_subtype** | **List[str]** |  | [optional] 
**biosample_type** | **List[str]** |  | [optional] 
**clinical** | **str** |  | [optional] 
**ethnicity** | **List[str]** |  | [optional] 
**experiment_accession** | **List[str]** |  | [optional] 
**expsample_accession** | **List[str]** |  | [optional] 
**gender** | **List[str]** |  | [optional] 
**sex** | **List[str]** |  | [optional] 
**max_subject_age** | **float** |  | [optional] 
**max_subject_age_gte** | **float** |  | [optional] 
**max_subject_age_lte** | **float** |  | [optional] 
**max_subject_age_gt** | **float** |  | [optional] 
**max_subject_age_lt** | **float** |  | [optional] 
**min_subject_age** | **float** |  | [optional] 
**min_subject_age_gte** | **float** |  | [optional] 
**min_subject_age_lte** | **float** |  | [optional] 
**min_subject_age_gt** | **float** |  | [optional] 
**min_subject_age_lt** | **float** |  | [optional] 
**measurement_technique** | **List[str]** |  | [optional] 
**planned_visit_accession** | **List[str]** |  | [optional] 
**race** | **List[str]** |  | [optional] 
**race_specify** | **List[str]** |  | [optional] 
**species** | **List[str]** |  | [optional] 
**strain** | **List[str]** |  | [optional] 
**study_accession** | **List[str]** |  | [optional] 
**study_time_collected** | **float** |  | [optional] 
**study_time_collected_gte** | **float** |  | [optional] 
**study_time_collected_lte** | **float** |  | [optional] 
**study_time_collected_gt** | **float** |  | [optional] 
**study_time_collected_lt** | **float** |  | [optional] 
**study_time_collected_unit** | **List[str]** |  | [optional] 
**study_time_t0_event** | **List[str]** |  | [optional] 
**study_time_t0_event_specify** | **List[str]** |  | [optional] 
**subject_accession** | **List[str]** |  | [optional] 
**study_title** | **List[str]** |  | [optional] 
**subject_phenotype** | **List[str]** |  | [optional] 
**treatment_accession** | **List[str]** |  | [optional] 
**format** | **str** |  | [optional] 

## Example

```python
from immport_client.models.filter_criteria_fields import FilterCriteriaFields

# TODO update the JSON string below
json = "{}"
# create an instance of FilterCriteriaFields from a JSON string
filter_criteria_fields_instance = FilterCriteriaFields.from_json(json)
# print the JSON string representation of the object
print(FilterCriteriaFields.to_json())

# convert the object into a dict
filter_criteria_fields_dict = filter_criteria_fields_instance.to_dict()
# create an instance of FilterCriteriaFields from a dict
filter_criteria_fields_from_dict = FilterCriteriaFields.from_dict(filter_criteria_fields_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


