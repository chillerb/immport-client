# LkAnalyte


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**analyte_accession** | **str** |  | [optional] 
**gene_symbol** | **str** |  | [optional] 
**gene_aliases** | **str** |  | [optional] 
**gene_id** | **str** |  | [optional] 
**genetic_nomenclature_id** | **str** |  | [optional] 
**immunology_symbol** | **str** |  | [optional] 
**link** | **str** |  | [optional] 
**official_gene_name** | **str** |  | [optional] 
**protein_ontology_id** | **str** |  | [optional] 
**protein_ontology_name** | **str** |  | [optional] 
**protein_ontology_synonyms** | **str** |  | [optional] 
**taxonomy_id** | **str** |  | [optional] 
**uniprot_entry** | **str** |  | [optional] 
**uniprot_entry_name** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_analyte import LkAnalyte

# TODO update the JSON string below
json = "{}"
# create an instance of LkAnalyte from a JSON string
lk_analyte_instance = LkAnalyte.from_json(json)
# print the JSON string representation of the object
print(LkAnalyte.to_json())

# convert the object into a dict
lk_analyte_dict = lk_analyte_instance.to_dict()
# create an instance of LkAnalyte from a dict
lk_analyte_from_dict = LkAnalyte.from_dict(lk_analyte_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


