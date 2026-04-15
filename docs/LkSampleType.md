# LkSampleType


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_sample_type import LkSampleType

# TODO update the JSON string below
json = "{}"
# create an instance of LkSampleType from a JSON string
lk_sample_type_instance = LkSampleType.from_json(json)
# print the JSON string representation of the object
print(LkSampleType.to_json())

# convert the object into a dict
lk_sample_type_dict = lk_sample_type_instance.to_dict()
# create an instance of LkSampleType from a dict
lk_sample_type_from_dict = LkSampleType.from_dict(lk_sample_type_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


