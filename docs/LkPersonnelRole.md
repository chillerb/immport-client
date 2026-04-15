# LkPersonnelRole


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_personnel_role import LkPersonnelRole

# TODO update the JSON string below
json = "{}"
# create an instance of LkPersonnelRole from a JSON string
lk_personnel_role_instance = LkPersonnelRole.from_json(json)
# print the JSON string representation of the object
print(LkPersonnelRole.to_json())

# convert the object into a dict
lk_personnel_role_dict = lk_personnel_role_instance.to_dict()
# create an instance of LkPersonnelRole from a dict
lk_personnel_role_from_dict = LkPersonnelRole.from_dict(lk_personnel_role_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


