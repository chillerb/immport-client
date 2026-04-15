# LkHmdb


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hmdb_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_hmdb import LkHmdb

# TODO update the JSON string below
json = "{}"
# create an instance of LkHmdb from a JSON string
lk_hmdb_instance = LkHmdb.from_json(json)
# print the JSON string representation of the object
print(LkHmdb.to_json())

# convert the object into a dict
lk_hmdb_dict = lk_hmdb_instance.to_dict()
# create an instance of LkHmdb from a dict
lk_hmdb_from_dict = LkHmdb.from_dict(lk_hmdb_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


