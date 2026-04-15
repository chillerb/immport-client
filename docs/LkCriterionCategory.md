# LkCriterionCategory


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_criterion_category import LkCriterionCategory

# TODO update the JSON string below
json = "{}"
# create an instance of LkCriterionCategory from a JSON string
lk_criterion_category_instance = LkCriterionCategory.from_json(json)
# print the JSON string representation of the object
print(LkCriterionCategory.to_json())

# convert the object into a dict
lk_criterion_category_dict = lk_criterion_category_instance.to_dict()
# create an instance of LkCriterionCategory from a dict
lk_criterion_category_from_dict = LkCriterionCategory.from_dict(lk_criterion_category_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


