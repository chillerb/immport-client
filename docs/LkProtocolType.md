# LkProtocolType


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_protocol_type import LkProtocolType

# TODO update the JSON string below
json = "{}"
# create an instance of LkProtocolType from a JSON string
lk_protocol_type_instance = LkProtocolType.from_json(json)
# print the JSON string representation of the object
print(LkProtocolType.to_json())

# convert the object into a dict
lk_protocol_type_dict = lk_protocol_type_instance.to_dict()
# create an instance of LkProtocolType from a dict
lk_protocol_type_from_dict = LkProtocolType.from_dict(lk_protocol_type_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


