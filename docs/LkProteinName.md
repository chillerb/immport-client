# LkProteinName


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**uniprot_id** | **str** |  | [optional] 
**uniprot_gene_name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_protein_name import LkProteinName

# TODO update the JSON string below
json = "{}"
# create an instance of LkProteinName from a JSON string
lk_protein_name_instance = LkProteinName.from_json(json)
# print the JSON string representation of the object
print(LkProteinName.to_json())

# convert the object into a dict
lk_protein_name_dict = lk_protein_name_instance.to_dict()
# create an instance of LkProteinName from a dict
lk_protein_name_from_dict = LkProteinName.from_dict(lk_protein_name_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


