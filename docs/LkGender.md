# LkGender


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_gender import LkGender

# TODO update the JSON string below
json = "{}"
# create an instance of LkGender from a JSON string
lk_gender_instance = LkGender.from_json(json)
# print the JSON string representation of the object
print(LkGender.to_json())

# convert the object into a dict
lk_gender_dict = lk_gender_instance.to_dict()
# create an instance of LkGender from a dict
lk_gender_from_dict = LkGender.from_dict(lk_gender_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


