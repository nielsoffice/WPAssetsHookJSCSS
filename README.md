# WPAssetsHookJSCSS
WordPress Hook for adding assets header and footer 

```PHP
 // This will goes to the header
 function addCss() { ?>
  <style>
    .wp_head_example { background-color : #f1f1f1; }
  </style>
 <?php }
 
add_action('wp_head', 'addCss');
```

```PHP
 // This will goes to the header
 function addJavaScript() { ?>
  <script>
    alert('Page is loading...');
   </script>
 <?php }
 
add_action('wp_head', 'addJavaScript');
```

```PHP
// Priority 
add_action( 'wp_head',  '_wp_render_title_tag',            1     );
add_action( 'wp_head',  'wp_enqueue_scripts',              1     );
add_action( 'wp_head',  'wp_resource_hints',               2     );
add_action( 'wp_head',  'feed_links',                      2     );
add_action( 'wp_head',  'feed_links_extra',                3     );
add_action( 'wp_head',  'rsd_link'                               );
add_action( 'wp_head',  'wlwmanifest_link'                       );
add_action( 'wp_head',  'adjacent_posts_rel_link_wp_head', 10, 0 );
add_action( 'wp_head',  'locale_stylesheet'                      );
add_action( 'wp_head',  'noindex',                          1    );
add_action( 'wp_head',  'print_emoji_detection_script',     7    );
add_action( 'wp_head',  'wp_print_styles',                  8    );
add_action( 'wp_head',  'wp_print_head_scripts',            9    );
add_action( 'wp_head',  'wp_generator'                           );
add_action( 'wp_head',  'rel_canonical'                          );
add_action( 'wp_head',  'wp_shortlink_wp_head',            10, 0 );
add_action( 'wp_head',  'wp_custom_css_cb',                101   );
add_action( 'wp_head',  'wp_site_icon',                    99    );
```

<br /> Source:
<br /> https://developer.wordpress.org/reference/hooks/wp_head/
<br /> https://developer.wordpress.org/reference/hooks/wp_footer/
