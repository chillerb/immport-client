# LkAgeEvent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_age_event import LkAgeEvent

# TODO update the JSON string below
json = "{}"
# create an instance of LkAgeEvent from a JSON string
lk_age_event_instance = LkAgeEvent.from_json(json)
# print the JSON string representation of the object
print(LkAgeEvent.to_json())

# convert the object into a dict
lk_age_event_dict = lk_age_event_instance.to_dict()
# create an instance of LkAgeEvent from a dict
lk_age_event_from_dict = LkAgeEvent.from_dict(lk_age_event_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


