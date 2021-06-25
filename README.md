# Home Assistant SVG File Loader

Use this to easily implement custom SVG Icons in Home Assistant. Unlike entity_picutre, this custom module will also update the icons color based on it's state.

# Instructions

1. Download & Copy Files

    copy ```file-loader.js``` to your ```/config/www``` folder and create a new folder ```svg``` inside ```www```. 
    Place your custom icons in ```svg```.

2. Add the Resource to Home Assistant

    Go to Configuration\Lovelace Dashboards\Resources and add a new resource. Enter ```/local/file-loader.js``` as URL.

# Usage

Specify custom icons like this ```file:your_icon_name``` where ```file``` is the namespace and ```your_icon_name``` is the filename of the SVG without the file extension.

# Customization

You may change the ```svg``` folders name to aynthing you want by changing this line:
```
const SVG_FOLDER_LOCATION = "/svg"
```

You may change the namespace to anything you like by changing this line:
```
const NAMESPACE = "file"
```

# Error Handling

If an invalid file path is specified, the module will automatically load a default icon containing a question mark.

If you want to override the default icon for certain entities, and not just the icon in a specific lovelace card, you will have to [setup customization](https://www.home-assistant.io/docs/configuration/customizing-devices/).

# Credits
Fallback icon is part of https://github.com/prasertcbs/HueIconPackPng/blob/master/LICENSE.

