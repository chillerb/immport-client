# LkOrganization


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_organization import LkOrganization

# TODO update the JSON string below
json = "{}"
# create an instance of LkOrganization from a JSON string
lk_organization_instance = LkOrganization.from_json(json)
# print the JSON string representation of the object
print(LkOrganization.to_json())

# convert the object into a dict
lk_organization_dict = lk_organization_instance.to_dict()
# create an instance of LkOrganization from a dict
lk_organization_from_dict = LkOrganization.from_dict(lk_organization_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


