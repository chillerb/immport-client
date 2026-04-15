# LkAdverseEventSeverity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_adverse_event_severity import LkAdverseEventSeverity

# TODO update the JSON string below
json = "{}"
# create an instance of LkAdverseEventSeverity from a JSON string
lk_adverse_event_severity_instance = LkAdverseEventSeverity.from_json(json)
# print the JSON string representation of the object
print(LkAdverseEventSeverity.to_json())

# convert the object into a dict
lk_adverse_event_severity_dict = lk_adverse_event_severity_instance.to_dict()
# create an instance of LkAdverseEventSeverity from a dict
lk_adverse_event_severity_from_dict = LkAdverseEventSeverity.from_dict(lk_adverse_event_severity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


