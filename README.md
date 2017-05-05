# wordpress-plugin-installer

The Connekt Plugin Installer is Class for displaying a list of recommended or required plugins inside of a users WordPress admin. 

The installer displays a list of plugins that users can easily install and activate directly for the screen they are currently viewing. 

![Connekt Plugin Installer Example](http://examples.connekthq.com/_gif/plugin-installer_2.gif)

This is a perfect tool for plugin and theme developers who want users to make it as easy as possible for users to install related plugins.


**Plugins must be available on the wordpress.org plugin repository to be installed and activated using this class**

To display a list of plugins you need to complete the following two steps:

### Class Loader
First step is to load the class into your plugin.  
```php
include_once('vendor/connekt-plugin-installer/class-connekt-plugin-installer.php');
```


### Display
Then build an array of plugin slugs and pass the array to the `Connekt_Plugin_Installer` class.

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