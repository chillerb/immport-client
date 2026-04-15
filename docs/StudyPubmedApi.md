# StudyPubmedApi


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pubmed_id** | **str** |  | [optional] 
**study_accession** | **str** |  | [optional] 
**authors** | **str** |  | [optional] 
**doi** | **str** |  | [optional] 
**issue** | **str** |  | [optional] 
**journal** | **str** |  | [optional] 
**month** | **str** |  | [optional] 
**pages** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**year** | **str** |  | [optional] 

## Example

```python
from immport_client.models.study_pubmed_api import StudyPubmedApi

# TODO update the JSON string below
json = "{}"
# create an instance of StudyPubmedApi from a JSON string
study_pubmed_api_instance = StudyPubmedApi.from_json(json)
# print the JSON string representation of the object
print(StudyPubmedApi.to_json())

# convert the object into a dict
study_pubmed_api_dict = study_pubmed_api_instance.to_dict()
# create an instance of StudyPubmedApi from a dict
study_pubmed_api_from_dict = StudyPubmedApi.from_dict(study_pubmed_api_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


