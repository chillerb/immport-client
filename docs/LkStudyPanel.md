# LkStudyPanel


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**collapsible** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**display_name** | **str** |  | [optional] 
**sort_order** | **int** |  | [optional] 
**visible** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_study_panel import LkStudyPanel

# TODO update the JSON string below
json = "{}"
# create an instance of LkStudyPanel from a JSON string
lk_study_panel_instance = LkStudyPanel.from_json(json)
# print the JSON string representation of the object
print(LkStudyPanel.to_json())

# convert the object into a dict
lk_study_panel_dict = lk_study_panel_instance.to_dict()
# create an instance of LkStudyPanel from a dict
lk_study_panel_from_dict = LkStudyPanel.from_dict(lk_study_panel_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


