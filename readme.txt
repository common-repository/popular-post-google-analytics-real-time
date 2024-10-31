=== Plugin Name ===
Contributors: vicenteguerra
Donate link: vicenteguerra.github.io
Tags: google analytics, trend, trendy, popular, posts, real time
Requires at least: 3.4
Tested up to: 3.4
Stable tag: 4.3
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Set Category with Popular Posts (Based in Google Analytics Real Time)

== Description ==

Get popular posts from Google Analytics Real Time and set every 10 minutes a new category called "Popular RT" with a number (By default 10 Posts) of popular post that you want and the number of active users in every post in this category, ready for you display your blog´s trendy post in every place of your Wordpress.

Query Example using the category and the number of views for sorting.

`<?php

$args = array( 'posts_per_page' => 5,
     'offset' => 0,
     'category_name' => 'popular_real_time_cat',
     'meta_key' => 'active_users',
     'orderby' => 'meta_value_num',
     'order' => 'DESC');

     $queryWP = new WP_Query();

 ?>`


*   The number of posts assigned in "Popular RT" may be less than the number selected (By default 10) because Google Analytics also include root path / (Home), categories or tags if have more active users than another posts.

== Installation ==

1. Upload the plugin files to the `/wp-content/plugins/popular-post-google-analytics-real-time` directory, or install the plugin through the WordPress plugins screen directly.
2. Activate the plugin through the 'Plugins' screen in WordPress
3. Use the Settings->Popular Post RT screen to configure the plugin


== Frequently Asked Questions ==

= How I can request access to Google Analytics Real Time? =

You only need fill the next information and in 24 hours with the correct configuration your connection to **Google Analytics Real Time API** should be work.

https://docs.google.com/forms/d/e/1FAIpQLSc9OpoDGB3tBD7oy1OG9fyum8KBIxs-2ihPCsHp13WTnM-SSQ/viewform

== Screenshots ==

![alt Plugin Settings](/assets/screenshot-1.png)
![alt Example](/assets/screenshot-2.png)
![alt Example Analytics](/assets/screenshot-3.png)

== Changelog ==

= 1.0 =
* Number of popular post configurable
* Test Connection to Google Analytics in Plugin Settings

== Upgrade Notice ==

= 1.0 =
Test your connection in Plugin Settings
