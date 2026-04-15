# LkTranscriptType


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_transcript_type import LkTranscriptType

# TODO update the JSON string below
json = "{}"
# create an instance of LkTranscriptType from a JSON string
lk_transcript_type_instance = LkTranscriptType.from_json(json)
# print the JSON string representation of the object
print(LkTranscriptType.to_json())

# convert the object into a dict
lk_transcript_type_dict = lk_transcript_type_instance.to_dict()
# create an instance of LkTranscriptType from a dict
lk_transcript_type_from_dict = LkTranscriptType.from_dict(lk_transcript_type_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


