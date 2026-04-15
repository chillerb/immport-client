# LkT0Event


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_t0_event import LkT0Event

# TODO update the JSON string below
json = "{}"
# create an instance of LkT0Event from a JSON string
lk_t0_event_instance = LkT0Event.from_json(json)
# print the JSON string representation of the object
print(LkT0Event.to_json())

# convert the object into a dict
lk_t0_event_dict = lk_t0_event_instance.to_dict()
# create an instance of LkT0Event from a dict
lk_t0_event_from_dict = LkT0Event.from_dict(lk_t0_event_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


