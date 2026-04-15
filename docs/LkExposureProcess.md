# LkExposureProcess


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 

## Example

```python
from immport_client.models.lk_exposure_process import LkExposureProcess

# TODO update the JSON string below
json = "{}"
# create an instance of LkExposureProcess from a JSON string
lk_exposure_process_instance = LkExposureProcess.from_json(json)
# print the JSON string representation of the object
print(LkExposureProcess.to_json())

# convert the object into a dict
lk_exposure_process_dict = lk_exposure_process_instance.to_dict()
# create an instance of LkExposureProcess from a dict
lk_exposure_process_from_dict = LkExposureProcess.from_dict(lk_exposure_process_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


