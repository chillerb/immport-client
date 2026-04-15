# LkRace


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_race import LkRace

# TODO update the JSON string below
json = "{}"
# create an instance of LkRace from a JSON string
lk_race_instance = LkRace.from_json(json)
# print the JSON string representation of the object
print(LkRace.to_json())

# convert the object into a dict
lk_race_dict = lk_race_instance.to_dict()
# create an instance of LkRace from a dict
lk_race_from_dict = LkRace.from_dict(lk_race_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


