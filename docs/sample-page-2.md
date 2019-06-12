# Another sample page

How about some `code`?

```php
function tainacan_blocks_get_plugin_js_settings(){
	global $TAINACAN_BASE_URL;

	$settings = [
		'root'     	=> esc_url_raw( rest_url() ) . 'tainacan/v2',
		'nonce'   	=> wp_create_nonce( 'wp_rest' ),
		'base_url' 	=> $TAINACAN_BASE_URL,
		'admin_url' => admin_url(),
		'site_url'	=> site_url(),
		'theme_items_list_url' => esc_url_raw( get_site_url() ) . '/' . \Tainacan\Theme_Helper::get_instance()->get_items_list_slug(),
	];

	return $settings;
}
```
