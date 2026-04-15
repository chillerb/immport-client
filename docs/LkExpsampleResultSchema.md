# LkExpsampleResultSchema


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**table_name** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_expsample_result_schema import LkExpsampleResultSchema

# TODO update the JSON string below
json = "{}"
# create an instance of LkExpsampleResultSchema from a JSON string
lk_expsample_result_schema_instance = LkExpsampleResultSchema.from_json(json)
# print the JSON string representation of the object
print(LkExpsampleResultSchema.to_json())

# convert the object into a dict
lk_expsample_result_schema_dict = lk_expsample_result_schema_instance.to_dict()
# create an instance of LkExpsampleResultSchema from a dict
lk_expsample_result_schema_from_dict = LkExpsampleResultSchema.from_dict(lk_expsample_result_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


