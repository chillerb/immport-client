# LkDisease


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 
**disease_ontology_id** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_disease import LkDisease

# TODO update the JSON string below
json = "{}"
# create an instance of LkDisease from a JSON string
lk_disease_instance = LkDisease.from_json(json)
# print the JSON string representation of the object
print(LkDisease.to_json())

# convert the object into a dict
lk_disease_dict = lk_disease_instance.to_dict()
# create an instance of LkDisease from a dict
lk_disease_from_dict = LkDisease.from_dict(lk_disease_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


