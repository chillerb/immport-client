# LkSourceType


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_source_type import LkSourceType

# TODO update the JSON string below
json = "{}"
# create an instance of LkSourceType from a JSON string
lk_source_type_instance = LkSourceType.from_json(json)
# print the JSON string representation of the object
print(LkSourceType.to_json())

# convert the object into a dict
lk_source_type_dict = lk_source_type_instance.to_dict()
# create an instance of LkSourceType from a dict
lk_source_type_from_dict = LkSourceType.from_dict(lk_source_type_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


