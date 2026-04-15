# StudyPubmed


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | [**StudyPubmedId**](StudyPubmedId.md) |  | [optional] 
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
from immport_client.models.study_pubmed import StudyPubmed

# TODO update the JSON string below
json = "{}"
# create an instance of StudyPubmed from a JSON string
study_pubmed_instance = StudyPubmed.from_json(json)
# print the JSON string representation of the object
print(StudyPubmed.to_json())

# convert the object into a dict
study_pubmed_dict = study_pubmed_instance.to_dict()
# create an instance of StudyPubmed from a dict
study_pubmed_from_dict = StudyPubmed.from_dict(study_pubmed_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


