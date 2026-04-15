# LkPublicRepository


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_public_repository import LkPublicRepository

# TODO update the JSON string below
json = "{}"
# create an instance of LkPublicRepository from a JSON string
lk_public_repository_instance = LkPublicRepository.from_json(json)
# print the JSON string representation of the object
print(LkPublicRepository.to_json())

# convert the object into a dict
lk_public_repository_dict = lk_public_repository_instance.to_dict()
# create an instance of LkPublicRepository from a dict
lk_public_repository_from_dict = LkPublicRepository.from_dict(lk_public_repository_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


