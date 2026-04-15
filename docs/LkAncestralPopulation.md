# LkAncestralPopulation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**abbreviation** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_ancestral_population import LkAncestralPopulation

# TODO update the JSON string below
json = "{}"
# create an instance of LkAncestralPopulation from a JSON string
lk_ancestral_population_instance = LkAncestralPopulation.from_json(json)
# print the JSON string representation of the object
print(LkAncestralPopulation.to_json())

# convert the object into a dict
lk_ancestral_population_dict = lk_ancestral_population_instance.to_dict()
# create an instance of LkAncestralPopulation from a dict
lk_ancestral_population_from_dict = LkAncestralPopulation.from_dict(lk_ancestral_population_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


