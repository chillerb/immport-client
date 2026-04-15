# LkSpecies


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**common_name** | **str** |  | [optional] 
**link** | **str** |  | [optional] 
**taxonomy_id** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_species import LkSpecies

# TODO update the JSON string below
json = "{}"
# create an instance of LkSpecies from a JSON string
lk_species_instance = LkSpecies.from_json(json)
# print the JSON string representation of the object
print(LkSpecies.to_json())

# convert the object into a dict
lk_species_dict = lk_species_instance.to_dict()
# create an instance of LkSpecies from a dict
lk_species_from_dict = LkSpecies.from_dict(lk_species_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


