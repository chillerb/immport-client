# LkVisibilityCategory


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_visibility_category import LkVisibilityCategory

# TODO update the JSON string below
json = "{}"
# create an instance of LkVisibilityCategory from a JSON string
lk_visibility_category_instance = LkVisibilityCategory.from_json(json)
# print the JSON string representation of the object
print(LkVisibilityCategory.to_json())

# convert the object into a dict
lk_visibility_category_dict = lk_visibility_category_instance.to_dict()
# create an instance of LkVisibilityCategory from a dict
lk_visibility_category_from_dict = LkVisibilityCategory.from_dict(lk_visibility_category_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


