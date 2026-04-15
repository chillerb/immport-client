# StudyPlannedVisitApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**planned_visit_accession** | **str** |  | [optional] 
**study_accession** | **str** |  | [optional] 
**end_rule** | **str** |  | [optional] 
**max_start_day** | **float** |  | [optional] 
**min_start_day** | **float** |  | [optional] 
**name** | **str** |  | [optional] 
**order_number** | **int** |  | [optional] 
**start_rule** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_planned_visit_api import StudyPlannedVisitApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyPlannedVisitApi from a JSON string
study_planned_visit_api_instance = StudyPlannedVisitApi.from_json(json)
# print the JSON string representation of the object
print(StudyPlannedVisitApi.to_json())

# convert the object into a dict
study_planned_visit_api_dict = study_planned_visit_api_instance.to_dict()
# create an instance of StudyPlannedVisitApi from a dict
study_planned_visit_api_from_dict = StudyPlannedVisitApi.from_dict(study_planned_visit_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


