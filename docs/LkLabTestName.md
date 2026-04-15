# LkLabTestName


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**cdisc_lab_test_code** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**lab_test_panel_name** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_lab_test_name import LkLabTestName

# TODO update the JSON string below
json = "{}"
# create an instance of LkLabTestName from a JSON string
lk_lab_test_name_instance = LkLabTestName.from_json(json)
# print the JSON string representation of the object
print(LkLabTestName.to_json())

# convert the object into a dict
lk_lab_test_name_dict = lk_lab_test_name_instance.to_dict()
# create an instance of LkLabTestName from a dict
lk_lab_test_name_from_dict = LkLabTestName.from_dict(lk_lab_test_name_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


