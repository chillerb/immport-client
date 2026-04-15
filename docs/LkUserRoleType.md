# LkUserRoleType


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_user_role_type import LkUserRoleType

# TODO update the JSON string below
json = "{}"
# create an instance of LkUserRoleType from a JSON string
lk_user_role_type_instance = LkUserRoleType.from_json(json)
# print the JSON string representation of the object
print(LkUserRoleType.to_json())

# convert the object into a dict
lk_user_role_type_dict = lk_user_role_type_instance.to_dict()
# create an instance of LkUserRoleType from a dict
lk_user_role_type_from_dict = LkUserRoleType.from_dict(lk_user_role_type_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


