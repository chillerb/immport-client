# StudyContractProgramApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**study_accession** | **str** |  | [optional] 
**contract_grant_id** | **int** |  | [optional] 
**contract_grant_category** | **str** |  | [optional] 
**contract_grant_description** | **str** |  | [optional] 
**contract_grant_end_date** | **str** |  | [optional] 
**external_id** | **str** |  | [optional] 
**contract_grant_link** | **str** |  | [optional] 
**contract_grant_name** | **str** |  | [optional] 
**contract_grant_start_date** | **str** |  | [optional] 
**program_id** | **int** |  | [optional] 
**program_category** | **str** |  | [optional] 
**program_description** | **str** |  | [optional] 
**program_end_date** | **str** |  | [optional] 
**program_link** | **str** |  | [optional] 
**program_name** | **str** |  | [optional] 
**program_short_name** | **str** |  | [optional] 
**program_start_date** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_contract_program_api import StudyContractProgramApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyContractProgramApi from a JSON string
study_contract_program_api_instance = StudyContractProgramApi.from_json(json)
# print the JSON string representation of the object
print(StudyContractProgramApi.to_json())

# convert the object into a dict
study_contract_program_api_dict = study_contract_program_api_instance.to_dict()
# create an instance of StudyContractProgramApi from a dict
study_contract_program_api_from_dict = StudyContractProgramApi.from_dict(study_contract_program_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


