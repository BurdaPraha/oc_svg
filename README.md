# SVG support for Opencart 2.x

Because jpg / png logo are retro!

## Installation

1. Requiring installed [Vqmod](https://github.com/vqmod/vqmod) because VqMod doesn't support installing via composer itself.
2. `composer require burdapraha/oc_svg dev-master`
3. Add this code to your composer.json project file:

```
    "scripts": {
        "post-install-cmd": [
            "php -r \"copy('vendor/burdapraha/oc_svg/vqmod/xml/svg_allow_upload.xml', 'upload/vqmod/xml/svg_allow_upload.xml');\""
        ],
        "post-update-cmd": [
            "php -r \"copy('vendor/burdapraha/oc_svg/vqmod/xml/svg_allow_upload.xml', 'upload/vqmod/xml/svg_allow_upload.xml');\""
        ]
    } 
```
    
It will move vqmod xml file to correct folder.

5. optionally you can add row to your `.gitignore` file with path to tracy.xml (example: upload/vqmod/xml/svg_allow_upload.xml)
6. celebrate!