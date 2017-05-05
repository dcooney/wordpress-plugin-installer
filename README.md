# wordpress-plugin-installer

A PHP Class for displaying a list of recommended or required plugins inside of the WordPress admin. 

**Plugins must be available on the wordpress.org plugin repository to be installed and activated using this class**

To display a list of plugins you need to complete the following two steps:

### Class Loader
First step is to load the class into your plugin.  
`include_once('vendor/connekt-plugin-installer/class-connekt-plugin-installer.php');`


### Display
Then build an array of plugin slugs and pass the array to the `Connekt_Plugin_Installer` class.

```
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