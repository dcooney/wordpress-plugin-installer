# wordpress-plugin-installer

The **Connekt Plugin Installer** is a Class for displaying a list of recommended or related plugins inside of the WordPress admin. 

The installer displays a list of plugins that users can easily install and activate from the screen they are currently viewing. 

![Connekt Plugin Installer Example](http://examples.connekthq.com/_gif/plugin-installer_2.gif)

This is a perfect tool for plugin and theme developers who wan to make it as easy as possible for users to install recommened plugins.

To see a live example, install a copy of [Ajax Load More](https://wordpress.org/plugins/ajax-load-more/) and go to the Extensions section.

***

## Getting Started

To start using this class you need to first load the class and then initialize the class as seen in the code samples below:


### Class Loader
First step is to load the class into your plugin or theme. This would typically appear in `functions.php` or in the `_construct` of your plugin Class.

```php
include_once('vendor/connekt-plugin-installer/class-connekt-plugin-installer.php');
```


### Display
Next, construct an array of plugin slugs and pass the array to the `init` method for display.

```php
$plugin_array = array(   			
  array(
    'slug' => 'ajax-load-more',
  ),
  array(
    'slug' => 'velocity',
  ),
  array(
    'slug' => 'instant-images'
  ),
  array(
    'slug' => 'easy-query'
  )
);
   			
if(class_exists('Connekt_Plugin_Installer')){
  Connekt_Plugin_Installer::init($plugin_array);
}
```

***

## Notes
- Plugins _must_ be available on the wordpress.org plugin repository to be installed and activated using this Class.


