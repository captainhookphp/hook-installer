# Hook-Installer

[![Latest Stable Version](https://poser.pugx.org/captainhook/hook-installer/v/stable.svg?v=1)](https://packagist.org/packages/captainhook/plugin-composer)
[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%208.0-8892BF.svg)](https://php.net/)
[![Downloads](https://img.shields.io/packagist/dt/captainhook/hook-installer.svg?v1)](https://packagist.org/packages/captainhook/plugin-composer)
[![License](https://poser.pugx.org/captainhook/hook-installer/license.svg?v=1)](https://packagist.org/packages/captainhook/plugin-composer)

`HookInstaller` is a `Composer Plugin` for [CaptainHook](https://github.com/captainhookphp/captainhook) it takes
care of activating your local git hooks.

For more information about `CaptainHook` visit the [Website](http://captainhook.info/).

## Installation:

As this is a composer-plugin you should use composer to install it.
 
```bash
$ composer require --dev captainhook/hook-installer
```

Everything else should happen automagically.

## Customize

You can set the path to your `CaptainHook` configuration file.
If you installed `CaptainHook` without using any of its Composer packages `captainhook/captainhook`
or `captainhook/captainhook-phar` you have to set the path to the executable.
All extra config settings are optional and if you are using the default settings you do not have to 
configure anything to make it work.
 
```json
{
  "extra": {
    "captainhook": {
      "config": "hooks.json",
      "exec": "tools/captainhook.phar",
      "disable-plugin": false
    }    
  }  
}

```

## A word of warning

It is still possible to commit without invoking the hooks. 
So make sure you run appropriate backend-sanity checks on your code!
