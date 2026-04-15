# LkExposureMaterial


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 
**exposure_material_id** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_exposure_material import LkExposureMaterial

# TODO update the JSON string below
json = "{}"
# create an instance of LkExposureMaterial from a JSON string
lk_exposure_material_instance = LkExposureMaterial.from_json(json)
# print the JSON string representation of the object
print(LkExposureMaterial.to_json())

# convert the object into a dict
lk_exposure_material_dict = lk_exposure_material_instance.to_dict()
# create an instance of LkExposureMaterial from a dict
lk_exposure_material_from_dict = LkExposureMaterial.from_dict(lk_exposure_material_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


