# LkPlateType


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_plate_type import LkPlateType

# TODO update the JSON string below
json = "{}"
# create an instance of LkPlateType from a JSON string
lk_plate_type_instance = LkPlateType.from_json(json)
# print the JSON string representation of the object
print(LkPlateType.to_json())

# convert the object into a dict
lk_plate_type_dict = lk_plate_type_instance.to_dict()
# create an instance of LkPlateType from a dict
lk_plate_type_from_dict = LkPlateType.from_dict(lk_plate_type_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


