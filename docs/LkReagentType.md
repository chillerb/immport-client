# LkReagentType


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_reagent_type import LkReagentType

# TODO update the JSON string below
json = "{}"
# create an instance of LkReagentType from a JSON string
lk_reagent_type_instance = LkReagentType.from_json(json)
# print the JSON string representation of the object
print(LkReagentType.to_json())

# convert the object into a dict
lk_reagent_type_dict = lk_reagent_type_instance.to_dict()
# create an instance of LkReagentType from a dict
lk_reagent_type_from_dict = LkReagentType.from_dict(lk_reagent_type_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


