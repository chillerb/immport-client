# StudyPubmedId


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**study_accession** | **str** |  | [optional] 
**pubmed_id** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_pubmed_id import StudyPubmedId

# TODO update the JSON string below
json = "{}"
# create an instance of StudyPubmedId from a JSON string
study_pubmed_id_instance = StudyPubmedId.from_json(json)
# print the JSON string representation of the object
print(StudyPubmedId.to_json())

# convert the object into a dict
study_pubmed_id_dict = study_pubmed_id_instance.to_dict()
# create an instance of StudyPubmedId from a dict
study_pubmed_id_from_dict = StudyPubmedId.from_dict(study_pubmed_id_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


