# LkVirusStrain


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**center_id_name_season_list** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 
**season_list** | **str** |  | [optional] 
**taxonomy_id** | **int** |  | [optional] 
**virus_name** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_virus_strain import LkVirusStrain

# TODO update the JSON string below
json = "{}"
# create an instance of LkVirusStrain from a JSON string
lk_virus_strain_instance = LkVirusStrain.from_json(json)
# print the JSON string representation of the object
print(LkVirusStrain.to_json())

# convert the object into a dict
lk_virus_strain_dict = lk_virus_strain_instance.to_dict()
# create an instance of LkVirusStrain from a dict
lk_virus_strain_from_dict = LkVirusStrain.from_dict(lk_virus_strain_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


