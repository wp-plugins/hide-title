=== Hide Title ===

Contributors: dojodigital
Plugin Name: Hide Title
Plugin URI: http://dojodigital.com/developer-tools/hide-title/
Tags: wp, title
Author URI: http://dojodigital.com/
Author: Dojo Digital
Requires at least: 3.0
Tested up to: 3.4.1
Stable tag: 1.0.1
Version: 1.0.1

Allows authors to hide the title on single pages and posts via the edit post screen.

== Description ==

This plugin allows the author of a post or page to hide the title and it's containing HTML element from the single view ( is_singular() ).
 
== Installation ==

1. Upload the `hide-title` folder to the `/wp-content/plugins/` directory
1. Activate the plugin through the 'Plugins' menu in WordPress

== Screenshots ==

1. This Meta Box will be added to the Edit screen for pages & posts

== Changelog == 

= 1.0.1 =

* Changed the jQuery to use a less brute force method of hiding the title. Added a set_selector() method to allow end-users to specify the css selector to hide. Tagged version 1.0.1

== Upgrade Notice == 

= 1.0.1 =

* This version uses a less brute force method of hiding the title by trying to find and hide `.entry-title` before looking for the title inside of `h1` or `h2` tags and hiding them. This version also adds a method for theme editors to change the selector from the default `.entry-title` to whatever they want to use.

== Frequently Asked Questions ==

= Hey! This plugin is hiding things I don't want hidden! =

By default this plugin looks for the `.entry-title` class and hides it. If it doesn't find it it will look for any `h1` or `h2` elements that contain the title and hide them instead. To change the default `.entry-title` selector to something that makes more sense to you, add the following code to the functions.php file of your current theme:

`global $DojoDigitalHideTitle;
// Be sure to replace ".your-selector" with your selector!
$DojoDigitalHideTitle->set_selector('.your-selector');`

As noted in the comments, you'll need to replace the string `.your-selector` with the css selector you'd like hidden. It can be any valid css selector such as `h1`, `.myclass`, `#myid`, etc. I recommend using a class or id to avoid accidentally hiding unforeseen elements.

= I don't want to edit my theme files, can't you just add an option page? =

I could, but I'd like to avoid adding Yet Another Options Page if I can. If enough people request it though, I'll go ahead and bite the bullet.





 