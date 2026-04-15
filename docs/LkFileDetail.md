# LkFileDetail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_file_detail import LkFileDetail

# TODO update the JSON string below
json = "{}"
# create an instance of LkFileDetail from a JSON string
lk_file_detail_instance = LkFileDetail.from_json(json)
# print the JSON string representation of the object
print(LkFileDetail.to_json())

# convert the object into a dict
lk_file_detail_dict = lk_file_detail_instance.to_dict()
# create an instance of LkFileDetail from a dict
lk_file_detail_from_dict = LkFileDetail.from_dict(lk_file_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


