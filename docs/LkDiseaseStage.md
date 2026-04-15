# LkDiseaseStage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_disease_stage import LkDiseaseStage

# TODO update the JSON string below
json = "{}"
# create an instance of LkDiseaseStage from a JSON string
lk_disease_stage_instance = LkDiseaseStage.from_json(json)
# print the JSON string representation of the object
print(LkDiseaseStage.to_json())

# convert the object into a dict
lk_disease_stage_dict = lk_disease_stage_instance.to_dict()
# create an instance of LkDiseaseStage from a dict
lk_disease_stage_from_dict = LkDiseaseStage.from_dict(lk_disease_stage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


