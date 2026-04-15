# LkSubjectLocation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_subject_location import LkSubjectLocation

# TODO update the JSON string below
json = "{}"
# create an instance of LkSubjectLocation from a JSON string
lk_subject_location_instance = LkSubjectLocation.from_json(json)
# print the JSON string representation of the object
print(LkSubjectLocation.to_json())

# convert the object into a dict
lk_subject_location_dict = lk_subject_location_instance.to_dict()
# create an instance of LkSubjectLocation from a dict
lk_subject_location_from_dict = LkSubjectLocation.from_dict(lk_subject_location_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


