Bootstrapwp - TWITTER BOOTSTRAP for WordPress
=================

Bootstrap is a responsive front-end toolkit from Twitter designed to kickstart web development, complete with core HTML, CSS, and JS for grids, type, forms, navigation, and many more components. Now you can use it with **WordPress** as a solid base to build custom themes quickly and easily.

Download the most-up-to-date theme files: [Download .zip file](https://github.com/downloads/rachelbaker/bootstrapwp-Twitter-Bootstrap-for-WordPress/bootstrapwp-87.zip)
Follow the development: [WIP Branch on Github](https://github.com/rachelbaker/bootstrapwp-Twitter-Bootstrap-for-WordPress/tree/1-WIP)

##Version .87 of BootstrapWP - still baking....

**The goals of this release are:**

1. ~~Switch to using the Less files instead of CSS~~

2. Add styling for wp_page_menu to navbar

2. ~~Improve navigation dropdown implementation~~

3. ~~Update styles and scripts to Bootstrap 2.04 release~~

4. ~~Switch to using bootstrap.js file instead of the separate .js files~~



__Functions.php__

*	Edited `bootstrapwp_css_loader()` function to use new `/less/bootstrapwp.css` generated from Less file compilation and removed references to previously used css files
*	Edited `bootstrapwp_js_loader()` function to include minified and minified bootstrap.min.js file
*	Edited `bootstrapwp_js_loader()` function to include `/js/bootstrapwp.demo.js` file containing all the extra JavaScript needed to enable the functionality of demos
*	Added new walker `Bootstrap_Walker_Nav_Menu` class to assign "dropdown-menu" class to navigation sub-menus

__Style.css__

*	Removed content because it this file is not loaded via `bootstrapwp_css_loader()` 
*	Added note to add custom updates to the less/bswp-custom.less file to safely retain the ability to update the less files with future versions of Bootstrap or BootstrapWP
*	Bumped version to .87

__Header.php__

*	Edited `wp_nav_menu()` call array to add `walker => new bootstrapwp_walker_nav_menu()` parameter
*	Removed extraneous commented line from `wp_nav_menu()` function call

__Footer.php__

*	Removed all Javascript and moved to new `js/bootstrapwp.demo.js` file

__Page-home.php__

*	Created file to be static homepage template that loads 3 widget areas (previously was index.php)

__Index.php__

*	Edited file to be standard blog homepage - and moved previous template content to new `page-home.php` file

__JS Folder__

*	Removed the individual .js files and replaced with single compiled `bootstrap.min.js` file
*   Added `bootstrap.js` (pre-minified version of bootstrap.min.js) file for reference
*   Added `bootstrapwp.demo.js` file which houses code is used to power all the JavaScript demos and examples for BootstrapWP
*   Added folder for google-code-prettify js and css files to style reference and documentation template files.

__CSS Folder__

*	Removed folder entirely because main style file is compiled less file located at `less/bootstrapwp.css`

__LESS Folder__

*	Updated LESS files from Twitter Bootstrap 2.04 branch
* 	Added `bswp-docs.less` file to pull in styles to allow doc pages to format correctly
*	Added note to use `bswp-custom.less` file for any custom additions to allow for easy updating of styles.
*	Added style fix for top positioning of scrollspy submenu to `less/bswp-overrides.less`

__IMG Folder__

*   Updated glyph icons with new set included in Bootstrap 2.04  


##Version .86 of BootstrapWP – Released April 11, 2012

**This release resolves a few major bugs and keeps the theme moving forward along with the progress of Twitter Bootstrap.**

The major changes are:

1. Removed the buggy catch_that_image function that was displaying thumbnails for posts, and replacing it with the new `bootstrapwp_autoset_featured_image()` function that will automatically set the post thumbnail.
2. Fixed navbar on mobile devices where body padding was causing the navbar to drop below the the top of the window.
3. Revised order of stylesheets loading
4. Corrected the broken favicon links

**[Download BootstrapWP .86 theme](https://github.com/downloads/rachelbaker/bootstrapwp-Twitter-Bootstrap-for-WordPress/bootstrapwp.zip)**


###Full Change Log


__Bootstrap Styles and Scripts__

*	Updated JS files from Bootstrap 2.0.3 branch as of April 7, 2012
*	Updated CSS files from Bootstrap 2.0.3 branch as of April 11, 2012
*	Updated LESS files from Bootstrap 2.0.3 branch as of April 7, 2012

__Functions.php__

*    Added `bootstrapwp_autoset_featured_image()` function to replace previous `catch_that_image()` function that was causing issues for some theme users.  The post thumbnail will now automatically be set to the first image added to a post if a featured image was not manually declared.
*	Edited `bootstrapwp_css_loader()` to move `/css/bootstrap-responsive.css` down in the loading order

__Page-blog.php__

*    Replaced `catch_that_image()` function with `the_post_thumbnail()`

__Author.php__

*    Replaced `catch_that_image()` function with `the_post_thumbnail()`

__Archive.php__

*    Replaced `catch_that_image()` function with `the_post_thumbnail()`

__Header.php__

*	Added `<?php bloginfo( 'template_url' );?>` to favicon link
*	Removed `get_header()` call at top of file

__Style.css__

*	Added `@media (max-width: 979px) { body { padding-top: 0; }` to correct navbar on mobile devices
*	Updated `.sub-menu` style to match `.dropdown-menu` from the Twitter Bootstrap styles to fix max-width restriction on navigation dropdown items

__Page-JSGuide.php__

*	Added content from Bootstrap 2.0.3 files
*	Added note about using the JS files within a WordPress theme

__Page-Styleguide.php__

*	Added content from Bootstrap 2.0.3 files

__Misc.__

*	Fixed JavaScript guide link in Readme thanks to @fsimmons
*	Updated favicons and moved them to /ico/ folder
*	Adding new screenshot image thanks to @yourdesigncoza



Demo
----
You can view a demo of this theme running on WordPress at:  [http://rachelbaker.me/bootstrapwp/](http://rachelbaker.me/bootstrapwp/)

View the theme style guide at: [http://rachelbaker.me/bootstrapwp/style-guide/](http://rachelbaker.me/bootstrapwp/style-guide/)

View the javascript guide at: [http://rachelbaker.me/bootstrapwp/javascript-guide/](http://rachelbaker.me/bootstrapwp/javascript-guide/)




Usage
-----

Download the BootstrapWP theme, and install to your WordPress site.

This is meant to be a base theme for WordPress custom theme development.

You can override any of the styles using style.css file.  All .css and .js files are loaded in functions.php.  Don't forget to disable any of the .js files you do not need.




Bug tracker
-----------
**Known theme bugs:**

Listed on the [Bug Tracker](http://rachelbaker.me/bootstrapwp/bug-tracker/) page

**Report additional bugs** [https://github.com/rachelbaker/bootstrapwp-Twitter-Bootstrap-for-WordPress/issues](https://github.com/rachelbaker/bootstrapwp-Twitter-Bootstrap-for-WordPress/issues)




Thanks to the Original Twitter Bootstrap Authors
-----------------------

**Mark Otto**

+ http://twitter.com/mdo
+ http://github.com/markdotto

**Jacob Thornton**

+ http://twitter.com/fat
+ http://github.com/fat


Copyright and license
---------------------


Licensed under the Apache License, Version 2.0 (the "License");
you may not use this work except in compliance with the License.
You may obtain a copy of the License in the LICENSE file, or at:

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
