# LkCellPopulation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**comments** | **str** |  | [optional] 
**definition** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_cell_population import LkCellPopulation

# TODO update the JSON string below
json = "{}"
# create an instance of LkCellPopulation from a JSON string
lk_cell_population_instance = LkCellPopulation.from_json(json)
# print the JSON string representation of the object
print(LkCellPopulation.to_json())

# convert the object into a dict
lk_cell_population_dict = lk_cell_population_instance.to_dict()
# create an instance of LkCellPopulation from a dict
lk_cell_population_from_dict = LkCellPopulation.from_dict(lk_cell_population_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


