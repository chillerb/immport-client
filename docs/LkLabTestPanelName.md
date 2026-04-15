# LkLabTestPanelName


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_lab_test_panel_name import LkLabTestPanelName

# TODO update the JSON string below
json = "{}"
# create an instance of LkLabTestPanelName from a JSON string
lk_lab_test_panel_name_instance = LkLabTestPanelName.from_json(json)
# print the JSON string representation of the object
print(LkLabTestPanelName.to_json())

# convert the object into a dict
lk_lab_test_panel_name_dict = lk_lab_test_panel_name_instance.to_dict()
# create an instance of LkLabTestPanelName from a dict
lk_lab_test_panel_name_from_dict = LkLabTestPanelName.from_dict(lk_lab_test_panel_name_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


