# FileDownloadURL


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**url** | **str** |  | [optional] 
**status** | **float** |  | [optional] 

## Example

```python
from immport_client.models.file_download_url import FileDownloadURL

# TODO update the JSON string below
json = "{}"
# create an instance of FileDownloadURL from a JSON string
file_download_url_instance = FileDownloadURL.from_json(json)
# print the JSON string representation of the object
print(FileDownloadURL.to_json())

# convert the object into a dict
file_download_url_dict = file_download_url_instance.to_dict()
# create an instance of FileDownloadURL from a dict
file_download_url_from_dict = FileDownloadURL.from_dict(file_download_url_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


