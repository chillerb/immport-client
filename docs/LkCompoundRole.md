# LkCompoundRole


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_compound_role import LkCompoundRole

# TODO update the JSON string below
json = "{}"
# create an instance of LkCompoundRole from a JSON string
lk_compound_role_instance = LkCompoundRole.from_json(json)
# print the JSON string representation of the object
print(LkCompoundRole.to_json())

# convert the object into a dict
lk_compound_role_dict = lk_compound_role_instance.to_dict()
# create an instance of LkCompoundRole from a dict
lk_compound_role_from_dict = LkCompoundRole.from_dict(lk_compound_role_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


