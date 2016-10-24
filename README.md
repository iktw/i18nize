# i18nize
This is a simple Client that integrates with the localization service www.i18nize.com

```pip install i18nize```


### Config parameters
| Name        | Type | Required | What? |
| ------------- |-------------|-------------|-------------|
| PROJECT_ID | String | Yes | This should be the id of your project. |
| DESTINATION_PATH | String | Yes | The path where you want your locale to get saved. |
| LIVE | Boolean | Yes | Set to *true* if you want to download your live locales otherwise your dev locales will get downloaded. |


### Example usage
```python
from i18nize.client import Client

client = Client(
    project_id='86416ce4-fd52-4daf-9764-46f35b07af23',
    destination_dir='locales/',
    live=False)

client.get_all_locales()

OUTPUT:
>> Downloaded en to dist/locales/en.json (live: True)
>> Downloaded sv to dist/locales/sv.json (live: True)
```