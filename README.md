# BreadcrumbsAuto
MediaWiki Breadcrumbs extension

If you find this useful or are using this in a commercial setting, please make a donation: https://www.paypal.me/kevin71246

INFO:
A MediaWiki can be created and structured many ways.  This extension creates breadcrumbs automatically if you use a given structure as defined below.  

The structure is as follows, as an example: 
-Starting with the Main Page, you create 3 additional pages (Page A, Page B, & Page C) using the [[New Page]] format on the Main Page.
-On Page A, you create 3 new pages: Page 1, Page 2, & Page 3

Breadcrumbs will automatically be created on Page 2 as such: 
Main Page > Page A > Page 2

It's certainly possible you may link from Page C to Page 2.  This will show up as an additional breadcrumb.  There is a setting to limit how many breadcrumbs get generated for a page.

Breadcrumbs will NOT show up for a page with any action (edit, creating new, etc), or for the Main page.

There are numerous settings.

IMPLEMENTATION:
-Copy BreadCrumbsAuto.php into extensions folder
-Add this line to LocalSettings.php:
   require_once('extensions/BreadCrumbsAuto.php');
   
OPTIONAL SETTINGS: (Add to LocalSettings.php)
$breadcrumbsAuto_DL = " > "; 												// Character to delimit the links in the breadcrumb
$breadcrumbsAuto_maxBreadcrumbs = 5; 								// Maximum number of links in breadcrumb (Main Page & Current page dont count)
$breadcrumbsAuto_maxBreadcrumbGroups = 5; 					// Maximum number of breadcrumb groups (entire line of breadcrumbs is 1 group)
$breadcrumbsAuto_maxPrefix = "[...]"; 							// Prefix if breadcrumb is longer than maxBreadcrumbs
$breadcrumbsAuto_prefix = "";												// Text to put before breadcrumb
$breadcrumbsAuto_currentPageLink = false;						// Show current page as a link
