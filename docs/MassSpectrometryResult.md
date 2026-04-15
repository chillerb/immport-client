# MassSpectrometryResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result_id** | **int** |  | [optional] 
**arm_accession** | **str** |  | [optional] 
**biosample_accession** | **str** |  | [optional] 
**comments** | **str** |  | [optional] 
**database_id_preferred** | **str** |  | [optional] 
**database_id_reported** | **str** |  | [optional] 
**experiment_accession** | **str** |  | [optional] 
**expsample_accession** | **str** |  | [optional] 
**intensity** | **float** |  | [optional] 
**mass_spectrometry_type** | **str** |  | [optional] 
**metabolite_name_preferred** | **str** |  | [optional] 
**metabolite_name_reported** | **str** |  | [optional] 
**protein_name_preferred** | **str** |  | [optional] 
**protein_name_reported** | **str** |  | [optional] 
**repository_accession** | **str** |  | [optional] 
**repository_name** | **str** |  | [optional] 
**retention_time** | **float** |  | [optional] 
**retention_time_unit** | **str** |  | [optional] 
**study_accession** | **str** |  | [optional] 
**study_time_collected** | **float** |  | [optional] 
**study_time_collected_unit** | **str** |  | [optional] 
**subject_accession** | **str** |  | [optional] 
**workspace_id** | **int** |  | [optional] 
**zcharge** | **str** |  | [optional] 
**mzratio** | **float** |  | [optional] 

## Example

```python
from immport_client.models.mass_spectrometry_result import MassSpectrometryResult

# TODO update the JSON string below
json = "{}"
# create an instance of MassSpectrometryResult from a JSON string
mass_spectrometry_result_instance = MassSpectrometryResult.from_json(json)
# print the JSON string representation of the object
print(MassSpectrometryResult.to_json())

# convert the object into a dict
mass_spectrometry_result_dict = mass_spectrometry_result_instance.to_dict()
# create an instance of MassSpectrometryResult from a dict
mass_spectrometry_result_from_dict = MassSpectrometryResult.from_dict(mass_spectrometry_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


