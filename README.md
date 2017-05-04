# wordpress-plugin-installer

A PHP Class for displaying a list of recommended or required plugins inside of the WordPress admin.


## Class Loader
Load the class...
`include_once('vendor/connekt-plugin-installer/class-connekt-plugin-installer.php');`


## DIsplay

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