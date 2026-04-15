# LkTimeUnit


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_time_unit import LkTimeUnit

# TODO update the JSON string below
json = "{}"
# create an instance of LkTimeUnit from a JSON string
lk_time_unit_instance = LkTimeUnit.from_json(json)
# print the JSON string representation of the object
print(LkTimeUnit.to_json())

# convert the object into a dict
lk_time_unit_dict = lk_time_unit_instance.to_dict()
# create an instance of LkTimeUnit from a dict
lk_time_unit_from_dict = LkTimeUnit.from_dict(lk_time_unit_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


