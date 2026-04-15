# LkResearchFocus


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_research_focus import LkResearchFocus

# TODO update the JSON string below
json = "{}"
# create an instance of LkResearchFocus from a JSON string
lk_research_focus_instance = LkResearchFocus.from_json(json)
# print the JSON string representation of the object
print(LkResearchFocus.to_json())

# convert the object into a dict
lk_research_focus_dict = lk_research_focus_instance.to_dict()
# create an instance of LkResearchFocus from a dict
lk_research_focus_from_dict = LkResearchFocus.from_dict(lk_research_focus_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


