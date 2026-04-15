# LkLocusName


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_locus_name import LkLocusName

# TODO update the JSON string below
json = "{}"
# create an instance of LkLocusName from a JSON string
lk_locus_name_instance = LkLocusName.from_json(json)
# print the JSON string representation of the object
print(LkLocusName.to_json())

# convert the object into a dict
lk_locus_name_dict = lk_locus_name_instance.to_dict()
# create an instance of LkLocusName from a dict
lk_locus_name_from_dict = LkLocusName.from_dict(lk_locus_name_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


